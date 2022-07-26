<template>
    <div class="header">
        <img src="../assets/img/logo-small.svg" alt="Spotify Logo">
    </div>
</template>

<script>
export default {
    name: "TheHeader",
}
</script>

<style lang="scss">
@import'../assets/Scss/style.scss';

.header {
    background-color: $secondary-color;
    height: 80px;

    img {
        line-height: 80px;
        height: 60px;
        display: block;
        margin-left: 20px;
        padding-top: 15px;
    }
}
</style>