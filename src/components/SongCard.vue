<template>
    <div class="song-card text-center">
        <img :src="poster" :alt="title" class="img-fluid">
        <h4>{{ title }}</h4>
        <p>{{ author }}<br>{{ year }}</p>
    </div>
</template>

<script>
export default {
    name: "SongCard",
    props: {
        title: String,
        poster: String,
        author: String,
        year: String
    }
}
</script>

<style lang="scss" scoped>
@import'../assets/Scss/style.scss';

.song-card {
    background-color: $secondary-color;
    height: 350px;
    width: calc(100% / 5 - 30px);
    margin: 50px 15px 15px 15px;

    img {
        padding: 15px;
    }

    h4 {
        font-weight: bold;
        color: #fff;
    }

    p {
        color: #666;
    }
}
</style>