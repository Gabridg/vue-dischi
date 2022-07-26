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
  background-color: $primary-color;
  height: 100vh;
}
</style>
