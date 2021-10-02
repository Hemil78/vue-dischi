<template>
  <header>
    <img src="../assets/images/spotify-logo.png" alt="logo-spotify">
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