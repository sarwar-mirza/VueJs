<script setup>
import { ref, reactive } from "vue";

const cl = ref('blue');
const bg = ref('yellow');


const myObj1 = reactive({
    color: 'green',
    backgroundColor: 'bisque',
})
const myObj2 = reactive({
    fontSize: '100px',
})

</script>

<template>
  <!-- inline style css -->
   <h1 style="color: red; background-color: bisque;">Style css-1 </h1>
   <h1 v-bind:style="{color: 'red', backgroundColor:'yellow'}">Binding Using CamealCase-2</h1>

   <h1 v-bind:style="{color: 'white', 'background-color': 'black'}">css for quotes-3</h1>

   <!-- Binding to object -->
    <h1 :style="{color:cl, backgroundColor:bg}">binding to object - 4</h1>
    <h1 :style="myObj1">call for object -5</h1>

    <!-- Binding to Array -->
    <h1 :style="[myObj1, myObj2]">Call for Array - 6</h1>
</template>

<style scoped>

</style>
