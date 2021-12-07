<template>
<div class="h-container">
    <img src="@/logo.png" alt="Spotify logo">
    <select v-model="changedGenre" @change="$emit('changeGenre', changedGenre)" name="genre" id="genre">
        <option value="Pop">Pop</option>
        <option value="Rock">Rock</option>
        <option value="Jazz">jazz</option>
        <option value="Metal">Metal</option>
    </select>
</div>
</template>

<script>
export default {
name: "Header",
data(){
    return{
        changedGenre:"",
    }
},
}
</script>

<style scoped lang="scss">
@import "@/scss/global";
    .h-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: $grey-bg;
        width: 100%;
        height: 10vh;
        padding: 10px;
        select{
            height:30px;
            background: white;
            padding: 5px;
        }
        img{
            height: 100%;
        }
    }
</style>