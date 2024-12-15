<script setup>
import Hello from './components/Hello.vue'

// Ex-03 import defaulte module
import { useCssModule } from 'vue';


// Ex-03 without Name
console.log(useCssModule());

// Ex-03 with Inject Name
// console.log(useCssModule("NameInject"));


</script>

<template>
  <Hello />

  <!-- calling Ex-01 css module -->
  <h1 :class="$style.bgColor">App Components (CSS module) </h1>

  <!-- calling Ex-02 Custom inject Name -->
   <!-- <h1 :class="NameInject.bgBlue">App Components (Custom inject Name)</h1> -->

</template>

<!-- Ex-01 (CSS Module)
 A <style module> tag is compiled as css Modules and exposes the resulting CSS
 class to the component as an object under the key of $style-->

<style module>
.bgColor{
    background-color: blueviolet;
}
</style>




<!-- Ex-02 - custom inject Name
 syntax: module="className"
 You can customize the property key of the injected classes object by giving the module attribute a value -->

<style module="NameInject">
.bgBlue{
  background-color: blue;
}
</style>

<!-- Ex -03(ex-01, 02)
 useCssModule()- it is used to access inject class -->
