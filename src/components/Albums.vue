<template>
    <div class="albums container mt-5">
        <div class="row row-cols-lg-5">
            <div class="card col-6 col-md-4" v-for="(album, index) in albums" :key="index">
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
            background-color: $lightColor;
        }
    }
</style>