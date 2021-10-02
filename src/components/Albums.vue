<template>
    <div class="albums container-md mt-5">
        <div class="row row-cols-lg-5">
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
            <div class="col-6 col-md-4 mb-3">
            <SingleAlbum/>
            </div>
        </div>
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
    .albums {
        display: flex;
        align-items: center;
    }
</style>