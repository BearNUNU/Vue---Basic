<template>
    <div>{{props.sendProps1}}</div>
    <div>{{props.sendProps2}}</div>
      <div>{{props.sendProps2.id}}</div>
       <div>{{props.sendProps2.name}}</div>
</template>

<script setup lang='ts'>
import { toRef } from "vue"

interface Props{
    sendProps1:string,
    sendProps2:object
}
const props = defineProps<Props>()
</script>

<style  scoped>

</style>