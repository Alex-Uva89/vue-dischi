<template>
  <header class="bg-primary">
      <div class="container d-flex justify-content-between align-items-center my-header">
      <div class="column-left">
          <i class="fa-brands fa-spotify"></i>
      </div>
      <div class="column-right">
      <search-album />
      </div>
      </div>
  </header>
</template>

<script>
import SearchAlbum from '@/components/SearchAlbum.vue'

export default {
    name: 'HeaderDischi',
    components: { SearchAlbum },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/style.scss';

.my-header{
    height: 3.5rem;
}

.column-left{
    filter: brightness(1);
    font-size: 2rem;
    color: $green-logo;
}
</style>