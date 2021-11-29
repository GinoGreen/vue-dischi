<template>
   <header>
      <img src="../assets/img/spotify-logo.png" alt="spotify logo">
      <Select @sendChange="$emit('sendChange', genr)"/>
   </header>
</template>

<script>
import Select from './Select.vue'

export default {
   name: 'Header',
   components: {
      Select
   }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   header {
      height: 70px;
      padding: 10px;

      @include center('align');
      justify-content: space-between;

      background-color: $card-color;

      img {
         height: 100%;
         cursor: pointer;
      }
   }
</style>