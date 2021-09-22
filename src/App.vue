 <template>
  <div>
  <Header />
  <AlbumList />
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
  }
}
</script>

<style lang="scss">
  @import "./styles/general.scss";
</style>
