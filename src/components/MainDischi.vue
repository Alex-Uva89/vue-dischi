<template>
  <main class="bg-secondary">
      <div class="container pt-5 pb-3">
      <div class="row row-cols-2 row-cols-md-3 row-cols-lg-4 row-cols-xl-5">
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


export default {
  components: { CardAlbum },
    name: 'MainDischi',
    
    component: {
        CardAlbum
    },
    
}
</script>

<style lang="scss" scoped>


</style>