<template>
   <main>

      <!-- loading -->
      <div v-if="isLoading" class="loading m-5">
         <Loading
            title="Caricamento albums..."
         />
      </div>

      <!-- albums -->
      <div v-else class="myContainer">
         <Album
            v-for="(album, index) in albums" :key="index"
            :album="album"
         />
      </div>

   </main>
</template>

<script>

import axios from 'axios';
import Loading from './Loading.vue';
import Album from './Album.vue';

export default {
   name: 'Main',
   components: {
      Album,
      Loading
   },
   data() {
      return {
         albums: [],
         isLoading: false,
         apiURL: 'https://flynn.boolean.careers/exercises/api/array/music'
      }
   },
   methods: {
      getApi() {

         this.isLoading = true;

         axios.get(this.apiURL)
            .then( response => {

               this.albums = response.data.response;
               this.isLoading = false;
            })
            .catch( error => {
               console.log(error);
            });
      }
   },
   mounted() {
      this.getApi();
   }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

$loading: 'true';

   main {
      height: calc(100% - 80px);

      @if $loading == 'false' { @include center(); }
      @else { @include center('justify') }

      overflow-y: auto;
      overflow-x: hidden;
      background-image: linear-gradient(
         lighten($primary-color, 4%),
         lighten($primary-color, 0%)
         );

      .myContainer {
         width: 1170px;
         margin: 0px auto;
         
         @include center();
         flex-wrap: wrap;

      }
   }

</style>