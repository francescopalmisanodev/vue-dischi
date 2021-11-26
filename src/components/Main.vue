<template>
<div class="m-container">
    <Card/>
</div>
</template>

<script>
import Card from './Card.vue';
export default {
    name:"Main",
    components: { 
    Card,
  }
}
</script>

<style scoped lang="scss">
    @import "@/scss/variables";
    .m-container {
        background-color:$blue-bg;
    }
</style>