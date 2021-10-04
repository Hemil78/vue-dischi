<template>
  <header>

    <div class="logo-spotify">
      <img src="../assets/images/spotify-logo.png" alt="logo-spotify">
    </div>

  </header>
</template>

<script>
export default {
    name: "Header",
    props: ['logo']
}
</script>

<style lang="scss" scoped>

@import "../assets/style/common";

header{
  background-color: $BGcolorHeader;
  padding: 8px;

  img{
    width: 60px;
  }
}


</style>