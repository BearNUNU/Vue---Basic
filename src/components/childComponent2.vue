<template>
    <div>
<button @click="sendEvent">버튼</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const data = ref<string>('자식컴포넌트의 데이터');
const emit = defineEmits(["send-event"]);
const sendEvent = () => {
    emit('send-event', data.value)
}

</script>
<style scoped>

</style>