<script setup>
import Helloworld from './components/HelloWorld.vue';   // calling component

const name = "Sarwar mithu";
</script>


<template>
    <div>
        <h1>Registration Form by {{name}}</h1>
        <Helloworld />    <!--define component -->
    </div>
</template>


<style scoped>
    
</style>