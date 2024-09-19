<script setup>
    import { ref } from 'vue';
    const count=ref(0);
    const increase=()=>{
      count.value+=1;
    }
</script>
<template>
    <div>
        <div>{{count}}</div>
        <button @click="increase">tăng</button> 
    </div>
</template>
