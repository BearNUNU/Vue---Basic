<template>
    <div>
<input type='text' v-model="inputValueA"/>
<input type='text' :value="inputValueB" @input="inputValueB = $event.target.value"/>
<h1>{{inputValueA}}</h1>
<h1>{{inputValueB}}</h1>
</div>
</template>

<script setup lang='ts'>
import { ref } from "vue";
const inputValueA = ref<Number>(0);
const inputValueB = ref<String>('');
</script>

<style  scoped>

</style>