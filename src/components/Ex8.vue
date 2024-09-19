<script setup>
import { ref } from 'vue';
const link = ref('https://www.google.com'); 
const check = () => {
  if (!link.value.startsWith('https://')) {
    alert('Đường dẫn không hợp lệ');
  } else {
     window.open(link.value, '_blank'); 
  }
};
</script>
<template>
  <div>
    <a :href="link" @click.prevent="check">{{ link }}</a>
  </div>
</template>
