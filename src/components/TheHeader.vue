<template>
    <div class="header">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center pt-2">
                <div class="col-6">
                    <img src="../assets/img/logo-small.svg" alt="Spotify Logo" class="img-fluid">
                </div>
                <div class="col-6 text-end">
                    <HeaderSelect :options="listMusic" @change-option="emitListMusic"> </HeaderSelect>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import HeaderSelect from './HeaderSelect.vue';
export default {
    name: "TheHeader",
    components: {
        HeaderSelect,
    },
    props: {
        listMusic: Array,
    },
    methods: {
        emitListMusic(genre) {
            this.$emit('change-genre', genre)
        }
    }
}
</script>

<style lang="scss">
@import'../assets/Scss/style.scss';

.header {
    background-color: $secondary-color;
    height: 80px;

    img {
        height: 50px;
        display: block;
        margin-left: 20px;
    }
}
</style>