<script setup>
import { ref } from 'vue';

const IsActive = ref(true);


</script>

<template>
    <!-- example-1 class attribute with component using is root directory -->
<!-- <h1 :class="{active: IsActive}">calling Component-1</h1> -->

<!-- Ex-02 onake gulo jodi directory thake ta hole kaj korbe na -->
 <!-- <h1 :class="{active : IsActive}">component don't work - 2</h1>
 <h1 :class="{active : IsActive}">component don't work - 3</h1> -->


<!-- ex-03 kaj korbe root directory te tar onake gulo child thakte pare -->
 <div>                    <!--call component class-->
    <h1 :class="{active: IsActive}">child -4</h1>
    <h1 :class="{active: IsActive}">child -5</h1>
 </div>


<!-- Ex-4 specific attribute jodi use korthe cai ($attrs.class) -->
<h1 :class="$attrs.class" class="text-red">using attribut using component-6</h1>

</template>

<style scoped>

</style>
