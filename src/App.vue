<template>
  <div id="main-wrapper">
    <Header/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss">

@import './assets/style/vars.scss';
@import './assets/style/general.scss';

#main-wrapper {
  height: 100vh;
}

</style>
