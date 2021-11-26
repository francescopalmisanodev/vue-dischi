<template>
  <div class="card">
      <h2>New Jersey</h2>
      <h3>Bon Jovi</h3>
      <h5>1988</h5>
      <h4>Rock</h4>
  </div>
</template>

<script>
export default {

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
    h2{
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