<template>
    <div class="albums container-md p-1 p-sm-2 p-md-3 p-lg-5">
        <div class="row row-cols-2 row-cols-md-4 row-cols-lg-5">
            <div class="card col my-2" v-for="(album, index) in filteredAlbums" :key="index">
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
    props : {
        passedGenre : String
    },
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
    },
    computed : {
        filteredAlbums() {
            const arrFiltered =  this.albums.filter(
                (elm) => {
                    if ( this.passedGenre == '' ) {
                        return this.albums;
                    } else {
                        return elm.genre.toLowerCase().includes(this.passedGenre.toLowerCase());
                    }
                    
                }
            );
            return arrFiltered;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';
    .row {
        display: flex;
        flex-wrap: wrap;
        padding: 1em 0;
    }

    .card {
        background-color: transparent;
        border: none;
    }
    
</style>