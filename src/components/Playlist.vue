<template>
  <section class="playlist">
      <Album/>
  </section>
</template>

<script>

import Album from './Album.vue';

export default {
    name: "Playlist",
    components: {
        Album
    }
}
</script>

<style lang="scss" scoped>

</style>