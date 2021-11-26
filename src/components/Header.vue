<template>
<div class="h-container">
    <img src="@/logo.png" alt="Spotify logo">
</div>
</template>

<script>
export default {
name: "Header",

}
</script>

<style scoped lang="scss">
@import "@/scss/global";
    .h-container {
        display: flex;
        justify-content: start;
        background: $grey-bg;
        width: 100%;
        height: 10vh;
        padding: 10px;
        img{
            height: 100%;
        }
    }
</style>