<template>
    <div class="song-card text-center">
        <img :src="image" :alt="title">
        <h4>{{ title }}</h4>
        <p>{{ autor }}<br>{{ year }}</p>
    </div>
</template>

<script>
export default {
    name: "SongCard",
    props: {
        title: String,
        image: String,
        author: String,
        year: String
    }
}
</script>

<style lang="scss">
@import'../assets/Scss/style.scss';

.song-card {
    background-color: $secondary-color;
    height: 350px;
    width: calc(100% / 5);
    margin-top: 50px;

    h4 {
        font-weight: bold;
        color: #fff;
    }

    p {
        color: #666;
    }
}
</style>