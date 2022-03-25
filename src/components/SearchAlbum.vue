<template>
<div>
  <select class="p-1" name="generi" id="">
        <option v-for="(genre, index) in genres" :key="index" value="genre[index]">{{ genre}}</option>       
    </select>
</div>
</template>

<script>
export default {
    name: 'SearchAlbum',
    data() {
        return {
            strSearch: '',
        },
        {
            genres:[
                '--scegli generi--',
                'rock',
                'jazz',
                'pop',
                'metal'
            ]
        }
    }
}
</script>

<style>

</style>