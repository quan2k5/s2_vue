<script setup>
import { ref } from 'vue'
const isDisable = ref(true) 
const text = ref('')
</script>
<template>
  <div>
    <input :disabled="isDisable" type="text" v-model="text" />
    <button @click="isDisable = !isDisable">
        Âns
    </button>
  </div>
</template>
