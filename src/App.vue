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
import axios from 'axios';


export default {
  name: 'App',
  data() {
        return {
            arrAlbum: null,
        }
    },
  components: {
    HeaderDischi,
    FooterDischi,
    MainDischi
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

<style lang="scss">
$primary: rgb(46,58,70);
$secondary: rgb(30,45,59);

@import "~bootstrap/scss/bootstrap";
</style>
