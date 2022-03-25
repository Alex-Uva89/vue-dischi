<template>
  <main class="bg-secondary">
      <div class="container pt-5 pb-3">
      <div class="row row-cols-2 row-cols-md-3 row-cols-lg-4 row-cols-xl-5">
          <card-album v-for="album in filterArray" 
            :key="album.title" 
            :album-data="album"
             />
      </div>
      </div>
  </main>
</template>

<script>
/* eslint-disable */
import CardAlbum from './CardAlbum.vue';


export default {
  components: { CardAlbum },
    name: 'MainDischi',
    props: {
           arrAlbum: Array,
           selectionGenre: String,
    },
    component: {
        CardAlbum
    },
    computed: {
      filterArray () {
        if ( this.selectionGenre === '') {
          return this.arrAlbum
        } else {
          return this.arrAlbum.filter(objGenre => objGenre.genre.includes(this.selectionGenre))
          
        }
      }   
    }
}
</script>

<style lang="scss" scoped>


</style>