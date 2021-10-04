<template>
  <div id="app">
    <Header :genreList="printedList" :authorsList="printedAuthor" :logoImg="require('./assets/images/spotify-logo.png')" @changedGenre="selectedGenre" @changedAuthor="selectedAuthor"/>
    <Albums @genresList="printList" :passedGenre="genre" @authorsList="printAuthors" :passedAuthor="author">
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
      printedList : [],
      author : '',
      printedAuthor : []
    }
  },
  methods : {
    selectedGenre(chosenGenre) {
      this.genre = chosenGenre;
    },
    printList(array) {
      this.printedList = array;
    },
    selectedAuthor(chosenAuthor) {
      this.author = chosenAuthor;
    },
    printAuthors(array) {
      this.printedAuthor = array;
    },
  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
