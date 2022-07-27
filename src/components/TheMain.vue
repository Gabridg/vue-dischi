<template>
    <div class="container d-flex flex-wrap">
        <SongCard v-for="song in songs" :key="song.title" :title="song.title" :poster="song.poster"
            :author="song.author" :year="song.year">

        </SongCard>
    </div>
</template>

<script>
import axios from "axios";
import SongCard from "./SongCard.vue"

export default {
    name: "TheMain",
    components: {
        SongCard,
    },
    data() {
        return {
            songs: [],
        }
    },
    mounted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
            this.songs = res.data.response
            console.log(res.data)
        })
    }
}
</script>

<style lang="scss" scoped>
@import'../assets/Scss/style.scss';

.container {
    max-width: 1200px;
    margin: 0 auto;
    box-sizing: border-box;
}
</style>
