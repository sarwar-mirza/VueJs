<script setup>
import Hello from './components/Hello.vue'

</script>

<template>
  <Hello />

  <h1 class="text-red bg-color">App Components</h1>
</template>

<style scoped>
.bg-color{
  background-color: blueviolet;
}

/* Global Selector
if you want just one rule to apply globally, you can use the :global() pseudo-class rather tan creating another */

:global(.text-red){
  color: brown;
}
</style>
