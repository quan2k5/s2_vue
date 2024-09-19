<script setup>
    const handleClick=()=>{
        console.log('click me');   
    }
</script>
<template>
    <div>
        <button @click="handleClick">Click me</button>
    </div>
</template>
