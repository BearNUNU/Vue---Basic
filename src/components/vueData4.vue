<template>
    <div>
        <childComponent :sendProps1="title" :sendProps2="obj" />
    </div>
</template>

<script setup lang="ts">
import { reactive, ref } from "vue";
import childComponent from "./childComponent.vue";
interface  Obj{
    id:Number,
    name:String
}

const title = ref<String>('string 타이틀')
const obj = reactive<Obj>({
    id:2020,
    name: 'john',
}) 
</script>

<style  scoped>

</style>