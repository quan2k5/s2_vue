<script setup>
import { ref } from 'vue';

const isActive = ref(tru);
const backgroundColor = ref('blue');
</script>

<template>
  <div>
    <div 
      :class="{ active: isActive }" 
      :style="{ backgroundColor: backgroundColor }" 
      class="block">
      Block
    </div>
  </div>
</template>

<style scoped>
.active{
  color: white;
}
</style>