<template>
    <header class="container">
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
@import '../assets/style/variables';

header {
    background-color: $lightColor;
    padding: 15px;
    height: 80px;
    display: flex;
}

</style>