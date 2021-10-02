<template>
    <div class="albums container-md mt-5">
        <div class="row row-cols-2 row-cols-md-3 row-cols-lg-5 g-2 g-lg-3">
            <div class="card col" v-for="(album, index) in albums" :key="index">
            <SingleAlbum :api="album"/>
            </div>
        </div>
    </div>
</template>

<script>
import SingleAlbum from './SingleAlbum.vue';
import axios from 'axios';
export default {
    name : "Albums",
    components : {
        SingleAlbum
    },
    data() {
        return {
            albums : []
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then( (response) => {
            this.albums = response.data.response;
        } );
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';
    .albums {
        display: flex;
        align-items: center;

        .row {
            width: 100%;
        }

        .card {
            background-color: transparent;
            border: none;
        }
    }
</style>