
<script setup>
import { ref } from 'vue';
const inputText = ref('');
const handleKey = (event) => {
  if (event.shiftKey && event.key === 'Enter') {
    alert(`Nội dung đã nhập: ${inputText.value}`);
    inputText.value = '';
  } else if (!event.shiftKey && event.key === 'Enter') {
    alert('Bạn cần nhấn Shift + Enter');
  }
};
</script>
<template>
  <div>
    <input
      type="text"
      v-model="inputText"
      @keyup.enter="handleKey"
      placeholder=""
    />
  </div>
</template>