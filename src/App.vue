<template>
  <div id="app">
    <Header :logoImg="require('./assets/images/spotify-logo.png')"/>
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
  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
