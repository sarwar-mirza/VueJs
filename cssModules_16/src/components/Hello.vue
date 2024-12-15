<script setup>
// v-bind in css Ex-04
// step-01
const theme = {textColor:"red"};
</script>

<template>
    <h1 class="text-red">Hello Components </h1>
</template>

<style scoped>

.text-red{
    /* step-02 */
    color: v-bind("theme.textColor");
}
</style>