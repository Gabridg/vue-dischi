<template>
  <div id="app">
    <Header></Header>
  </div>
</template>

<script>
import Header from "./components/TheHeader.vue";

export default {
  name: 'App',
  components: {
    Header,

  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';

#app {
  background-color: #1e2d3b;
  height: 100vh;
}
</style>
