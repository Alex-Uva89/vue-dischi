<template>
  <main class="bg-secondary">
      <div class="my-space-card">
          <card-album />
      </div>
  </main>
</template>

<script>
import CardAlbum from './CardAlbum.vue'


export default {
  components: { CardAlbum },
    name: 'MainDischi',
    component: {
        CardAlbum
    }
}
</script>

<style lang="scss" scoped>

</style>