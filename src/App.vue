<template>
  <div class="container">
    <Header/>
    <Main :songs="songs" />
  </div>
</template>

<script>
import axios from "axios";
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  data(){
    return{songs:[],}
  },
  created() {
    this.getMusic();
  },
  methods:{
    getMusic(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
      .then(result =>{
      this.songs=result.data.response;
      console.log(this.songs);
      } )
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

