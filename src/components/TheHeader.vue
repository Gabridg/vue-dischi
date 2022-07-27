<template>
    <div class="header">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center pt-2">
                <div class="col-6">
                    <img src="../assets/img/logo-small.svg" alt="Spotify Logo" class="img-fluid">
                </div>
                <div class="col-6 text-end">
                    <select name="" id="">
                        <option value="" hidden>Genere Musicale</option>
                        <option value="rock">Rock</option>
                        <option value="pop">Pop</option>
                        <option value="jazz">Jazz</option>
                        <option value="metal">Metal</option>
                    </select>
                </div>
            </div>
        </div>
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
        height: 50px;
        display: block;
        margin-left: 20px;
    }

    select {
        width: 35%;
        height: 25%;
    }
}
</style>