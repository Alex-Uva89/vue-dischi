<template>
  <header class="bg-primary">
      <div class="container d-flex justify-content-between align-items-center my-header">
      <div class="column-left">
          <i class="fa-brands fa-spotify"></i>
      </div>
      <div class="column-right">
          <select class="p-1" name="generi" id="">
              <option value="all">--seleziona generi--</option>
              <option value="rock">rock</option>
              <option value="jazz">jazz</option>
              <option value="pop">pop</option>
              <option value="metal">metal</option>
          </select>
      </div>
      </div>
  </header>
</template>

<script>


export default {
    name: 'HeaderDischi'
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