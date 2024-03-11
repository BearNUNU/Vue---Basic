<template>
    <div>
        {{ rawHtml }}
        {{ rawHtml2 }}
        <h1 v-html="rawHtml2"></h1>
        <h2 v-bind:class="{ active: isActive }">클래스 바인딩</h2>
        <h2 :class="{ active: isActive }">클래스 바인딩</h2>
        <button @click="onChange"> 버튼</button>
        <h3 style="color:green">스타일 바인딩</h3>
        <h3 :style="{color:textColor}">스타일 바인딩</h3>
        <h3></h3>       
    </div>
</template>

<script setup>
import { ref } from "vue";

const rawHtml = "이것은 텍스트입니다.";
const rawHtml2 = '<span style="color: red;">v-html</span>';
const isActive = ref(true);
let textColor = 'red';
const onChange = () => {
    isActive.value = !isActive.value;
    console.log(isActive.value);
}
</script>

<style scoped>
h2{
    color:black;
}
h2.active { 
    color: blue;
}

</style>