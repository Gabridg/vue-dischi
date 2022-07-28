<template>
  <div id="app">
    <Header :list-music="listMusic" @change-genre="setGenre"></Header>
    <Main :selected-genre="selectedGenre" @sinc-songs="setListGenre"></Main>
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
  },
  data() {
    return {
      selectedGenre: "",
      listMusic: [],
    }
  },
  methods: {
    setGenre(genre) {
      this.selectedGenre = genre;
    },
    setListGenre(genres) {
      this.listMusic = genres;
    }
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
