<template>
    <div>
<h1>{{text}}</h1>
<h1>{{changeText()}}</h1>
<h1>{{changeText()}}</h1>
<h1>{{changeText()}}</h1>
<h1>{{changeTextB}}</h1>
<h1>{{changeTextB}}</h1>
<h1>{{changeTextB}}</h1>
    </div>
</template>

<script setup>
//함수처럼 코드를 작성하지만 리턴 시키는 데이터를 사용해서 데이터 취급하는 복잡한 로직을 미리 처리하는 계산된 형태의 속성, 캐싱기능

import { ref, computed } from 'vue';

const text = ref("computed 데이터 문구");

const changeText = () => {
    console.log("함수호출", text);
    const a = text.value;
    return a.split('').reverse().join('')
}

const changeTextB = computed(() => {
    console.log("컴퓨티드 호출", text.value);
    const a = text.value;
    return a.split('').reverse().join('');
});
//changeTextB는 로그에 한번만 호출되는게 보임 (캐싱)
</script>

<style scoped>

</style>