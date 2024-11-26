<!-- Method and computed -->
<script setup>
import { ref } from 'vue';

let firstName = ref("Sadiya")
let lastName = ref("Sarwar")

// method without parameter
// function fullName() {
//     return firstName.value+ " "+lastName.value;
// }

// setTimeout(() => {
//     console.log("SetTimeOut Called");
//     lastName.value = "Mirza";
// }, 2000);


// method without parameter
function fullName(dept) {                              // accepet parameter
    return firstName.value+ " "+lastName.value +" " + "is a " + dept;
}

setTimeout(() => {                                 
    console.log("SetTimeOut Called");
    lastName.value = "Mirza";
}, 2000);

</script>

<template>
    <!--<h1>{{ fullName() }}</h1>-->     <!--without parameter-->
    <h1>{{ fullName("Doctor") }}</h1>     <!--passing with parameter-->
</template>

<style scoped>

</style>