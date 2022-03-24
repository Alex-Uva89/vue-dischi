<template>
  <div id="app">
    <header-dischi />
    <main-dischi />
    <footer-dischi />
  </div>
</template>

<script>
import HeaderDischi from './components/HeaderDischi.vue';
import FooterDischi from './components/FooterDischi.vue';
import MainDischi from './components/MainDischi.vue';
import "../assets/variables.scss";

export default {
  name: 'App',
  components: {
    HeaderDischi,
    FooterDischi,
    MainDischi
  }
}
</script>

<style lang="scss">
$primary: rgb(46,58,70);
$secondary: rgb(30,45,59);

@import "~bootstrap/scss/bootstrap";
</style>
