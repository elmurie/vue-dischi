<template>
    <header>
        <img :src="logoImg" alt="Logo">
        <select v-model="selectOption" @change="$emit('changedGenre', selectOption)">
            <option value="" disabled selected hidden>Select a genre</option>
            <option value="">All</option>
            <option value="Rock">Rock</option>
            <option value="Metal">Metal</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
        </select>
    </header>
</template>

<script>
export default {
    name : "Header",
    props : ['logoImg'],
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