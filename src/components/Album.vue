<template>
   <div class="album">
      <div class="album-image">
         <img src="" alt="">
      </div>
      <div class="album-title">
         <h3 class="text-center m-0"></h3>
      </div>
      <div class="album-author">
         <p class="text-center m-0"></p>
         <span class="text-center"></span>
      </div>
   </div>
</template>

<script>
export default {
   name: 'Album'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   .album {
      height: 300px;
      width: calc(100% / 5 - 40px);
      margin: 10px 20px;
      padding: 10px;

      background-color: $card-color;

      .album-image {
         height: 45%;
         overflow-y: hidden;

         img {
            width: 100%;
         }
      }
      .album-title {
         height: 35%;
      }
      .album-author {
         height: 20%;
      }
   }
   
</style>