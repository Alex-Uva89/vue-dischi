<template>
  <main class="bg-secondary">
      <div class="container p-5">
      <div class="row row-cols-lg-5">
          <card-album v-for="(album, index) in arrAlbum" 
            :key="index" 
            :album-data="album"
             />
      </div>
      </div>
  </main>
</template>

<script>
import CardAlbum from './CardAlbum.vue';
import axios from 'axios';

export default {
  components: { CardAlbum },
    name: 'MainDischi',
    data() {
        return {
            arrAlbum: null,
        }
    },
    component: {
        CardAlbum
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => {
            console.log(result.data)
            this.arrAlbum = result.data.response
        })
    }
}
</script>

<style lang="scss" scoped>


</style>