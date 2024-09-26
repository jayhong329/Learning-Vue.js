<script setup>
import { ref } from 'vue';
const message = ref("響應式互動")
</script>


<template>
    <div>
        <h2>My Second Component 這是第二個組件</h2>
        <p>Composition APIs</p>
        <input type="text" v-model="message">
        <p>{{ message }}</p>
    </div>
</template>
<style scoped>
h2{
    color: blue;
}
</style>