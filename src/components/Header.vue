<template>
  <header class="d-flex align-items-center justify-content-between">
    <a href="/">
    <img src="https://www.wallpapertip.com/wmimgs/17-176153_download-logo-spotify-png.png" alt="Logo Spotify">
    </a>

    <select name="genre" id="genre" class="form-select" @click="$emit('performSelect', selectedInput)" v-model="selectedInput">
      <option value="">Seleziona Genere</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </header>
</template>

<script>
export default {
  name: 'Header',
   data() {
    return {
      selectedInput:""
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/vars';

  header {
    background-color: $sec;
    height: 70px;
    padding: 10px;

    a,
    a img {
      height: 100%;
    }
  }

  select {
  font-size: 20px;
  padding: 5px 10px;
  border: 1px solid white;
  border-radius: 10px;
  text-align: center;
  background-color: $bg;
  color: white;
  width: 200px;

    option {
      font-size: 18px;
      background-color: $sec;
    }
}

</style>
