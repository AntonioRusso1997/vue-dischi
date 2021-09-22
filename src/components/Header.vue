<template>
  <header>
    <a href="/">
    <img src="https://www.wallpapertip.com/wmimgs/17-176153_download-logo-spotify-png.png" alt="Logo Spotify">
    </a>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/vars';

  header {
    background-color: $sec;
    height: 70px;
    padding: 10px;
    img {
      height: 100%;
    }
  }

</style>
