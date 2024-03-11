<template>
  <div>
    <buttom v-on:click="count++"> 인라인 핸들러</buttom>
    <h1>{{ count }}</h1>
    <button v-on:click="changeName">메소드 핸들러</button>
    <h1>{{ name }}</h1>
  </div>
</template>

<script setup>
import { ref } from "vue"
const count = ref(0)
const name = ref("vue.js")
const changeName = () => {
  name.value = "변경된 텍스트 데이터 입니다."
}
</script>

<style scoped></style>
