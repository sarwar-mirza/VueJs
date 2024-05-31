<script setup>

    const mydata = "mithu";
    const url = "https://www.linkedin.com/in/sarwar-mithu/";

    const objdata = {
        id: "sadiya",
        href: "https://www.linkedin.com/in/sarwar-mithu/",
    };

    const attributeName = "href";

</script>

<template>
    <!-- Attribute Bindings v-bind -->
    <h1 :id="mydata">Sarwar mithu -1</h1> <br>
    <a :href="url">Linkedin Profile</a> <br>

    <h3 v-bind="objdata">call all attribute</h3> <br>

    <!-- Dynamic Argument -->
    <a v-bind:[attributeName]="url">Dynamic Argument</a>
</template>


<style scoped>

</style>