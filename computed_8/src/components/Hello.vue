<!-- Computed property (read only) -->

<!-- <script setup>
import { ref, computed } from 'vue';

const firstName = ref("Sadiya")
const lastName = ref("Mirza")

// method 
// function fullName() {
//     return firstName.value + " " + lastName.value
// }


// computed property
const fullName = computed( () => {
  console.log("Getter called")
  return firstName.value + " " + lastName.value
})



setTimeout(() => {
  console.log("SetTimeOut called ")
  lastName.value = "Sarwar"
}, 2000);


</script>

<template>
  <h1>{{ fullName }}</h1>
</template>

<style scoped>

</style> -->






<!-- Writeable Computed property(when using read and write) -->

<script setup>
import { ref, computed } from 'vue';

const firstName = ref("Sadiya");
const lastName = ref("Mirza");


// Computed property

const fullName = computed({
  // call getter  (read only)
  get() {
    console.log("Getter called")
    return firstName.value + " " + lastName.value;
  },

  // call setter  (write only)
  set(newValue) {
    console.log("setter Called")
    // Note: we are using destructuring assignment syntax here.
    [firstName.value, lastName.value]=newValue.split(" ")
    
  },
});

setTimeout(() => {
  console.log("SetTimeOut called")
  fullName.value = 'Aaira Baby'
}, 2000);

</script>

<template>
  <h1>{{ fullName }}</h1>
</template>

<style scoped></style>