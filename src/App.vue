<template>
  <div id="app">
    <Header :logoImg="require('./assets/images/spotify-logo.png')" @changedGenre="selectedGenre"/>
    <Albums>
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
      genre : ''
    }
  },
  methods : {
    selectedGenre(chosenGenre) {
      this.genre = chosenGenre;
      console.log('select field passed this genre to app.vue', this.genre);
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
