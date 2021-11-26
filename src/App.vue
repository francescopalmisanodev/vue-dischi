<template>
  <div class="container">
    <Header/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
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

