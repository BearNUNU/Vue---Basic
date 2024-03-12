<template>
    <div>
        <h1>{{ text }}</h1>
        <button v-on:click="changeMessage">텍스트 변경</button>
    </div>
</template>

<script setup>
import { ref, watch } from "vue";

const text = ref("watch 기능 테스트, 오리지널 문구");
const changeCheck = ref(false);
watch(() => {
    window.alert('변경 감지');
}, { immediate: true });

const changeMessage = () => {
    console.log('함수 호출 확인');
    console.log(changeCheck.value);
    changeCheck.value = !changeCheck.value;

    if (changeCheck.value === true) {
        text.value = '텍스트 변경 완료';
    } else {
        text.value = "watch 기능 테스트, 오리지널 문구";
    }
}
</script>

<style scoped>
</style>
