<template>
    <header>
        <img :src="logoImg" alt="Logo">
        <select v-model="selectOption" @change="$emit('changedGenre', selectOption)">
            <option value="" selected>All</option>
            <option v-for="(genre, index) in genreList" :key="index" :value="genre">{{genre}}</option>
        </select>
        <select v-model="selectAuthor" @change="$emit('changedAuthor', selectAuthor)">
            <option value="" selected>All</option>
            <option v-for="(author, index) in authorsList" :key="index" :value="author">{{author}}</option>
        </select>
    </header>
</template>

<script>
export default {
    name : "Header",
    props : ['logoImg', 'genreList', 'authorsList'],
    data() {
        return {
            selectOption : "",
            selectAuthor : ""
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