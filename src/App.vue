<template>
  <div id="app">
    <Header/>
    <Playlist/>
  </div>
</template>

<script>

import Header from './components/Header.vue';
import Playlist from './components/Playlist.vue';


export default {
  name: 'App',
  components: {
    Header,
    Playlist,
  }
}
</script>

<style lang="scss">

@import './assets/style/common.scss';

#app{
  background-color: $BGcolorBody;
}

</style>
