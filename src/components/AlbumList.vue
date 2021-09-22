<template>
  <div class="container mt-5 mb-5">
    <div v-if="!load" class="row">
      <div v-for="(album, index) in albumList" :key="index" class="my-col col-lg-3 col-md-4 col-sm-12 mt-4">
        <AlbumCard :alb="album" /> 
      </div>  
    </div>
    <Loader v-else />
  </div>
</template>

<script>
import axios from 'axios';
import AlbumCard from './AlbumCard.vue'
import Loader from './Loader.vue'

export default {
  name: 'AlbumList',
  components: {
    AlbumCard,
    Loader
  },
   data() {
    return {
      albumList: [],
      APIUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
      load: true
    }
  },
  created() {
    this.getAlbum();
  },
  methods: {
    getAlbum() {
      axios
          .get(this.APIUrl)
          .then( result => {
            console.log(result.data.response);
            this.albumList = result.data.response;
            // this.load = false;
            setTimeout( () => {this.load = false; }, 5000);
          })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .container {
    width: 60%;
  }
  
  @media screen and (min-width: 1530px) {
  .my-col {
    width: calc((100% / 5) - 10px);
    margin: 5px;
  }
  }
</style>
