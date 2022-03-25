<template>
  <div id="app">
    <header-dischi 
    @sendGenre="selectGenere"
    :arrGenres="arrGenres"
     />
    <main-dischi 
    :selectionGenre= valueSelection
    :arrAlbum="arrAlbum"
     />
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
            arrGenres: [],
            valueSelection: '',
        }
    },
  components: {
    HeaderDischi,
    FooterDischi,
    MainDischi
  },
   methods: {
    selectGenere (value) {
      this.valueSelection = value
      console.log(this.valueSelection)
    }
  },
  
  created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => {
            this.arrAlbum = result.data.response
            for (let album = 0; album < this.arrAlbum.length; album++) {
              if (!this.arrGenres.includes(this.arrAlbum[album].genre)) {
                this.arrGenres.push(this.arrAlbum[album].genre)
              }  
          }
        })
    },
    
}
</script>

<style lang="scss">
$primary: rgb(46,58,70);
$secondary: rgb(30,45,59);

@import "~bootstrap/scss/bootstrap";
</style>
