<template>
    <header>
        <img :src="logoImg" alt="Logo">
    </header>
</template>

<script>
export default {
    name : "Header",
    props : ['logoImg']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';

header {
    background-color: $lightColor;
    padding: .625rem;
    height: 3.125rem;
    display: flex;

    img {
        height: 100%;
    }
}

</style>