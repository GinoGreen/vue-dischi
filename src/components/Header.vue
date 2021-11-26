<template>
   <header>
      <img src="../assets/img/spotify-logo.png" alt="spotify logo">
   </header>
</template>

<script>
export default {
   name: 'Header'
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';

   header {
      height: 80px;
      padding: 10px;

      background-color: $card-color;

      img {
         height: 100%;
         cursor: pointer;
      }
   }
</style>