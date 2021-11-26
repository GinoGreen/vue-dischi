<template>
   <main>
      <div class="container">
         <Album/>
      </div>
   </main>
</template>

<script>

// import axios from 'axios';
import Album from './Album.vue';

export default {
   name: 'Main',
   components: {
      Album
   }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';

   main {
      height: calc(100% - 80px);
      overflow-y: auto;
      background-color: $primary-color;
   }

</style>