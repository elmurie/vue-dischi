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
    padding: 15px;
    height: 5rem;
    display: flex;
}

</style>