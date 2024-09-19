<script setup>
    const handleClick=(str)=>{
        console.log(str);    
    }
</script>
<template>
    <div>
        <button @click="()=>{handleClick('rikkei academy')}">Click</button>
    </div>
</template>