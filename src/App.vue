<template>
  <div class="container">
    <Header @changeGenre="filterGenre"/>
    <Main :songs="filtredSongs" />
  </div>
</template>

<script>
import axios from "axios";
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  data(){
    return{songs:[],
    filtredSongs:[],}
  },
  created() {
    this.getMusic();
  },
  methods:{
    getMusic(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
      .then(result =>{
      this.songs=result.data.response;
      this.filtredSongs=result.data.response;
      } )
    },
    filterGenre(changedGenre){
     this.filtredSongs=this.songs.filter(song => song.genre===changedGenre);
    }
  },
  components: { 
    Header,
    Main,
  }
}
</script>

<style lang="scss">
  @import "@/scss/global";
    .container {
      display: flex;
      flex-direction: column;
      Main{
        flex-grow: 1;
      }
    }
</style> 

