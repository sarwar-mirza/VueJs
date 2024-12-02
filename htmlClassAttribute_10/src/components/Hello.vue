<script setup>
import {ref, reactive, computed} from 'vue';

// Bindit to object
const IsActive = ref(true);  // IsActive = ref(false) jodi hoy ta hole attribute classes dekhabe na
const IsImportant = ref(true);

const classObj = reactive({
    IsActive: true,
    'f-bold': true,
    IText: true
});

// computed property
const myClass = computed( () => ({
    active : IsActive.value,
    'f-bold': IsImportant.value
}));


// Binding to array
const currentTabBg = ref("bg-green");
const errorClass = ref("text-red")
</script>

<template>
<h1 class="text-red">Normal HTML Attribute-1</h1>

<!-- Binding to object -->
 <h1 v-bind:class="{active: IsActive}">Passing to object v-bind:class -2</h1>
 <h1 :class="{active: IsActive}">Passing to object v-bind:class -3</h1>

 <h1 class="text-red" :class="{active: IsActive}">Class and normal class attribute togather-4</h1>
 <h1 :class="{active: IsActive, fBold: IsImportant}">Class and normal class attribute togather-5</h1>
 <h1 :class="{active: IsActive, 'f-bold': IsImportant}">Class and normal class attribute togather using single quotes-6</h1>

 
 
 <h1 :class="classObj">Reactive object in class-7</h1>
 
 <!-- Computed -->
  <h1 :class="myClass">Computed property in class -8</h1>

  <!-- Binding to array -->
   <h1 :class="[currentTabBg, errorClass]">Bind :class to an array -9</h1>

<!-- condition class -->
 <h1 :class="[IsActive ? currentTabBg : '', errorClass]">condition in class - 10</h1>
 <h1 :class="[{'bg-black': IsActive}, errorClass]">condition in class - 11</h1>

</template>

<style scoped>

</style>