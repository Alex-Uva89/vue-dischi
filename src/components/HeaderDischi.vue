<template>
  <header class="bg-primary">
      <div class="container d-flex justify-content-between align-items-center my-header">
      <div class="column-left">
          <i class="fa-brands fa-spotify"></i>
      </div>
      <div class="column-right">
      
      <select v-model="searchGenres" @change="$emit('sendGenre', searchGenres)" class="p-1" name="generi" id="genres-search">
          <option value="all">tutti</option>
          <option v-for="genre in arrGenres" :key="genre" :value="genre">{{ genre }}</option>       
      </select>
      </div>
      </div>
  </header>
</template>

<script>


export default {
    name: 'HeaderDischi',
    props:{
        arrGenres: Array,
    },
    data() {
        return {
            searchGenres: '',
        }
    }
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