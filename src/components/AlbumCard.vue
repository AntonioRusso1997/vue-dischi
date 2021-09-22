<template>
  <div class="card">
    <img :src="alb.poster" alt="alb.title">
    <h2 class="text-white mt-3 mb-3">{{alb.title}}</h2>
    <h3 class="text-gray fs-5 mb-0">{{alb.author}}</h3>
    <p class="">{{alb.year}}</p>
  </div>
</template>

<script>
export default {
  name: 'AlbumCard',
  props: ["alb"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/vars';

.card {
  background-color: $sec;
  min-height: 370px;
  text-align: center;
  padding: 20px;
  cursor:pointer;

  img {
    width: 100%;
  }

  h2 {
    text-transform: uppercase;
    font-size: 22px;
    font-weight: 700;
  }

  h3,
  p {
    color: gray;
  }
  
}
</style>
