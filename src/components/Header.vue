<template>
    <header>
        <img :src="logoImg" alt="Logo">
        <select v-model="selectOption" @change="$emit('changedGenre', selectOption)">
            <option value="" selected>All</option>
            <option v-for="(genre, index) in genreList" :key="index" :value="genre">{{genre}}</option>
            
        </select>
    </header>
</template>

<script>
export default {
    name : "Header",
    props : ['logoImg', 'genreList'],
    data() {
        return {
            selectOption : ""
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';

header {
    background-color: $lightColor;
    padding: .625rem;
    height: 3.125rem;
    display: flex;
    justify-content: space-between;

    img {
        height: 100%;
    }
}

</style>