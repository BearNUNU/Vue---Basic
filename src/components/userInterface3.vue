<template>
  <div>
    <li>{{ sampleArr[0] }}</li>
    <li v-for="item in sampleArr" :key="item">{{ item }}</li>
    <li v-for="user in userArr" :key="user.id">{{ user.id + user.name }}</li>
  </div>
</template>

<script setup>
const sampleArr = ["a", "b", "c", "d"]
const userArr = [
  { id: 1, name: "a" },
  { id: 2, name: "b" },
  { id: 3, name: "c" },
  { id: 4, name: "d" },
]
</script>

<style scoped></style>
