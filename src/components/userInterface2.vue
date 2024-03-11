<template>
    <div>
        <div v-if="isVisivle" class="red"></div>
        <div v-if="isVisivle ===true " class="blue"></div>
        <div v-else class="green"></div>
        <div v-show="isVisivle === false" class="gray"></div>
        <button @click="onChange">버튼</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
const isVisivle = ref(false);
const onChange = () => {
    isVisivle.value = !isVisivle.value
}

</script>

<style scoped>
.red{
    width: 100px;
    height: 100px;
    background-color: red;
}
.blue{
  width: 100px;
    height: 100px;
    background-color: blue;
}
.green{
  width: 100px;
    height: 100px;
    background-color: green;
}
.gray{
     width: 100px;
    height: 100px;
    background-color: gray; 
}

</style>