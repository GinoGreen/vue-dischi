<template>
   <main>
      <div class="myContainer">
         <Album/>
         <Album/>
         <Album/>
         <Album/>
         <Album/>
         <Album/>
         <Album/>
      </div>
   </main>
</template>

<script>

import axios from 'axios';
import Album from './Album.vue';

export default {
   name: 'Main',
   components: {
      Album
   },
   data() {
      return {
         albums: [],
         apiURL: 'https://flynn.boolean.careers/exercises/api/array/music'
      }
   },
   methods: {
      getApi() {
         axios.get(this.apiURL)
            .then( (response) => {
               console.log(response);
            })
            .catch( error => {
               console.log(error);
            });
      }
   },
   mounted() {
      this.getApi;
   }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   main {
      height: calc(100% - 80px);

      @include center();

      overflow-y: auto;
      overflow-x: hidden;
      background-color: $primary-color;

      .myContainer {
         width: 1170px;
         margin: 0px auto;
         
         @include center();
         flex-wrap: wrap;

      }
   }

</style>