<template>
  <div class="col text-center px-3" :id="albumData.genre">
      <div class="bg-primary p-3 mb-3 my-card">
      <img class="img-fluid" :src="albumData.poster" :alt="albumData.title">
      <h2 class="fs-5 mt-2 text-white">{{ albumData.title }}</h2>
      <h3 class="fs-6 my-color">{{ albumData.author }}</h3>
      <div class="my-color">{{ albumData.year }}</div>
      </div>
  </div>
</template>

<script>
export default {
    props: {
        albumData: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/style.scss';


.my-card{
    height: 20rem;
    .my-color:{
        color: $black-text
    }
}

</style>