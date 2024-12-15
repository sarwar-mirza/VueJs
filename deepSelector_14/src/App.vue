<script setup>
import Hello from './components/Hello.vue'

</script>

<template>
  <Hello />
</template>

<style scoped>
  /* .bg-color{
    background-color: blueviolet;
   } */

  /* DeepSelectore */
  .bg-color,
  :deep(.bg-color){
    background-color: brown;
  }

   
</style>
