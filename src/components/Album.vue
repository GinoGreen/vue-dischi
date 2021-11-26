<template>
   <div class="album">
      <div class="album-image">
         <img :src="album.poster" alt="">
      </div>
      <div class="album-title">
         <p class="text-center fw-bold">{{ album.title }}</p>
      </div>
      <div class="album-author">
         <p class="text-center m-0">{{ album.author }}</p>
         <p class="text-center">{{ album.year }}</p>
      </div>
   </div>
</template>

<script>
export default {
   name: 'Album',
   props: {
      album: Object
   }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   .album {
      height: 300px;
      width: calc(100% / 5 - 40px);
      margin: 10px 20px;
      padding: 20px;

      background-color: $card-color;

      p {
         margin: 0;
         color: #807F7F;
      }

      .album-image {
         height: 50%;
         overflow-y: hidden;

         img {
            width: 100%;
         }
      }
      .album-title {
         height: 35%;
         
         @include center('both');

         p {
            font-size: 1.3rem;
            color: #fff;
         }
      }
      .album-author {
         height: 15%;
         display: flex;
         flex-direction: column;
         align-items: center;
         justify-content: flex-end;

         p {
            line-height: 16px;
         }
      }
   }
   
</style>