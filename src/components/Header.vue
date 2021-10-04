<template>
    <header>
        <img :src="logoImg" alt="Logo">
        <div class="filters">
            <select v-model="selectOption" @change="$emit('changedGenre', selectOption)">
                <option value="" selected disabled hidden>Filter by genre</option>
                <option value="">All</option>
                <option v-for="(genre, index) in genreList" :key="index" :value="genre">{{genre}}</option>
            </select>
            <select class="ms-3" v-model="selectAuthor" @change="$emit('changedAuthor', selectAuthor)">
                <option value="" selected disabled hidden>Filter by author</option>
                <option value="">All</option>
                <option v-for="(author, index) in authorsList" :key="index" :value="author">{{author}}</option>
            </select>
        </div>
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