<script setup>
import { ref } from 'vue'
const elementId = ref('scdv')
const elementClass = ref('heading')
</script>
<template>
  <div id="app">
    <h1 :elementId="elementId" :elementClass="elementClass">Heading</h1>
  </div>
</template>
<style scoped>

</style>