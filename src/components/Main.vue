<template>
<div class="m-container">
    <Card v-for="song in songs" :key="song.title" :author="song.author" :title="song.title" :poster="song.poster" :genre="song.genre" :year="song.year"/>
</div>
</template>

<script>
import Card from './Card.vue';
export default {
    name:"Main",
    components: { 
    Card,
  },
  props: {
      songs: Array,
  }
}
</script>

<style scoped lang="scss">
    @import "@/scss/variables";
    .m-container {
        background-color:$blue-bg;
        display: flex;
        flex-wrap: wrap;
    }
</style>