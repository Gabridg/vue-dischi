<template>

    <select v-model="optionSelect" @change="changeOption">
        <option value="" hidden>Genere Musicale</option>
        <option v-for="option in options" :key="option" :value="option">{{ option }}</option>
    </select>
</template>

<script>

export default {
    name: "HeaderSelect",
    data() {
        return {
            optionSelect: "",
        };
    },
    props: {
        options: Array,
    },
    methods: {
        changeOption() {
            this.$emit('change-option', this.optionSelect);
        }
    }
}
</script>

<style lang="scss">
@import '../assets/Scss/style.scss';

select {
    width: 35%;
    height: 25%;
}
</style>