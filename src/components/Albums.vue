<template>
    <div class="albums container">
        <SingleAlbum/>
    </div>
</template>

<script>
import SingleAlbum from './SingleAlbum.vue'
export default {
    name : "Albums",
    components : {
        SingleAlbum
    }
}
</script>

<style lang="scss" scoped>

</style>