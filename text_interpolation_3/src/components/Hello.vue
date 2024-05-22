<script setup>
    const msg = "Learning by Text Interpolation";    // properties
    const num = 30;         // properties
    const on = true;        // properties

    function disp() {      // methods
        console.log("Learn Text interpolation")
    }
</script>


<template>
    <h1>{{msg}}</h1><br>            <!--properties Text interpolation-->
    <h1>{{num + 10}}</h1><br>       <!--properties Text interpolation-->
    <h1>{{on? 'Dark' : 'Light'}}</h1>   <!--properties Text interpolation-->
    <h1>{{ disp() }}</h1>               <!--method Text interpolation-->
</template>


<style scoped>

</style>