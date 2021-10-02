<template>
    <div class="album text-center p-3">
        <div class="wrapper">
            <img :src="api.poster" :alt="api.title">
            <h3 class="my-4">{{api.title}}</h3>
            <h4 class="m-0">{{api.author}}</h4>
            <h4>{{api.year}}</h4>
        </div>
    </div>
</template>

<script>
export default {
    name : "SingleAlbum",
    props : {
        api : Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';
    .album, .wrapper {
        background-color: $lightColor;
        height: 100%;
        img {
            width: 100%;
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