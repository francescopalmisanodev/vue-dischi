<template>
  <div class="card">
      <img :src="poster" :alt="title">
      <h2>{{title}}</h2>
      <h3>{{author}}</h3>
      <h5>{{year}}</h5>
      <h4>{{genre}}</h4>
  </div>
</template>

<script>
export default {
name:"Card",
props: {
    author: String,
    genre: String,
    poster: String,
    title: String,
    year: String,
}
}
</script>

<style scoped lang="scss">
@import "@/scss/variables";
.card {
    width: calc(100%/8);
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 20px;
    text-align: center; 
    img{
        width: 100%;
    }
    h2{
        font-size:1.25rem;
        color: white;
        padding: 0.3em;
        
    }
    h3,h5 {
        color:$grey-txt;
        padding: 0.3em;
    }
    h4 {
        color: white;
        padding: 0.3em;
    }
}

</style>