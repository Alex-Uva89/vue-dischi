<template>
  <header class="bg-primary">
      <div class="container d-flex justify-content-between align-items-center my-header">
      <div class="column-left">
          <i class="fa-brands fa-spotify"></i>
      </div>
      <div class="column-right">
          <select name="generi" id="">
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
@import '../assets/variables.scss';

.my-header{
    height: 3rem;
}

.column-left{
    color: $green-logo;
    filter: brightness(50);
    font-size: 2rem;
}
</style>