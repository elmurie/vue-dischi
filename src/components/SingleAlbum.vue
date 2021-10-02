<template>
    <div class="album text-center p-4">
        <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        <h3 class="m-3">NEW JERSEY</h3>
        <h4 class="m-0">Bon Jovi</h4>
        <h4 class="mb-5">1988</h4>
    </div>
</template>

<script>
export default {
    name : "SingleAlbum"
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';
    .album {
        background-color: $lightColor;

        img {
            max-width: 100%;
        }
        h3 {
            font-size: $titleFontSize;
            text-transform: uppercase;
        }
        h4 {
            color: $accentText;
            font-size: $dataFontSize;
            font-weight: 400;
        }
    }

</style>