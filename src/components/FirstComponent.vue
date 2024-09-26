<script setup>
import { onBeforeMount, onMounted } from 'vue';

onBeforeMount(() =>{
    console.log("before-mount")
})
onMounted(() =>{
    console.log("mounted")
    const myH = document.querySelector("#theH")
    console.log(myH.textContent)
})

</script>
<template>
    <h2 id="theH">My First Component 這是第一個組件</h2>
</template>
<style scoped>
h2{
    color: forestgreen;
}
</style>