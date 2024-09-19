<script setup>
const onSubmit=()=>{
    alert('Form submission prevented!');
}
    
</script>
<template>
    <form @submit.prevent='onSubmit'>
        <p>FORM</p>
        <input type="text">
        <button type="submit">Submit</button>
    </form>
</template>
