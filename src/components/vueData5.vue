<template>
    <div>
<childComponent2 @send-event="parentEvent"/>
    </div>
</template>

<script setup lang="ts">
import childComponent2 from "./childComponent2.vue"
const parentEvent = (event: string) =>{
    console.log(event)
}

</script>

<style scoped>

</style>