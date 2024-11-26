<script setup>
import { reactive, ref, isRef } from 'vue';

const a = ref(10)
setTimeout( () =>{
    console.log("a", a);
    console.log("a.value", a.value)
    a.value++;
    console.log("is a Ref:", isRef(a));
}, 2000);
</script>

<template>
    <h1>Count: {{ a }}</h1>
</template>


<style scoped></style>