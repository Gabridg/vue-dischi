<template>
  <div id="app">
    <Header></Header>
    <Main></Main>
  </div>
</template>

<script>
import Header from "./components/TheHeader.vue";
import Main from "./components/TheMain.vue";

export default {
  name: 'App',
  components: {
    Header,
    Main,

  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';

#app {
  background-color: $primary-color;
  height: 100vh;
}
</style>
