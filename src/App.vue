<template>
  <div id="app">
    <Header :genreList="printedList" :logoImg="require('./assets/images/spotify-logo.png')" @changedGenre="selectedGenre"/>
    <Albums @genresList="printList" :passedGenre="genre">
      <SingleAlbum/>
    </Albums>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Albums from './components/Albums.vue'
import SingleAlbum from './components/SingleAlbum.vue'

export default {
  name: 'App',
  components: {
    Header,
    Albums,
    SingleAlbum
  },
  data() {
    return {
      genre : '',
      printedList : []
    }
  },
  methods : {
    selectedGenre(chosenGenre) {
      this.genre = chosenGenre;
    },
    printList(array) {
      this.printedList = array;
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
