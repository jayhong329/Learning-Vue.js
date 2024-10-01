<script setup>
import { ref } from 'vue';
     const isLogin = ref(false);
     const getName = () => "Jack";

     const i = ref(0) ;
     const week = ["日", "一", "二", "三", "四", "五", "六"]
     const author = ref({
        books: [
        'Vue 2 - Advanced Guide',
        'Vue 3 - Basic Guide',
        'Vue 4 - The Mystery'
    ]
     })


     const id = ref(10)
     const homeUrl = "http://www.google.com.tw"
     const isDisabled = ref(true)


</script>

<template>
    <div>
        <h2>第三個組件 {{ getName() }}</h2>
        <p>{{ isLogin ? "yes" : "no" }}</p>
        <hr>
        <!--錯誤寫法 <p>{{ if (true) {rerturn "Hello"} }}</p> -->
        <p>{{ new Date().toLocaleDateString() }}</p>
        <!--錯誤寫法 <p>{{ let name = 'Jack’ }}</p> -->
        <p>{{ i+1 }}</p>
        <!--錯誤寫法 <p>{{ i+=1 }}</p> -->
        <p>星期{{week[2]}}</p>
        <p>星期{{week[new Date().getDay()]}}</p>
        <p>出版了書籍：{{author.books.length > 0 ? '是':'否'}}</p>
        <hr>
        <!-- 屬性繫節 -->
        <p>ID: {{ id }}</p>
        <hr>
        <button :disabled = "isDisabled" >click</button>
    </div>
</template>

<style lang="css" scoped>

</style>