 <template>
  <div>
  <Header @performSelect="getGenre" />
  <AlbumList :filterGen="selectedInput" />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import AlbumList from './components/AlbumList.vue'

export default {
  name: 'App',
  components: {
    Header,
    AlbumList
  },
  data() {
    return {
      selectedInput:""
    }
  },
  methods: {
    getGenre(text) {
      this.selectedInput = text;
    }
  }
}
</script>

<style lang="scss">
  @import "./styles/general.scss";
</style>
