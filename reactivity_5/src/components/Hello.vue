<script setup>
    import { reactive, ref } from "vue"        // reactive(), ref()
    const num = reactive({a:15, b:25});

    // setTimeout( () => {
    //     console.log("SetTimeOut Called");
    //     console.log("Num", num);
    //     num.a = 10
    //     console.log("Num.a", num.a);
    //     console.log("Num.b", num.b);

    // }, 2000);


    // const obj = reactive({count:0});
    // setTimeout( () => {
    //     console.log("SetTimeOut called");
    //     console.log("obj", obj);
    //     obj.count++;
    // }, 2000);


    // Deep reactivity


    const obj1 = reactive({
        num: {count:0},
        user:["sadya", "sarwar"],
    })

    // setTimeout( () => {
    //     console.log("obj1", obj1);
    //     console.log("obj1.num", obj1.num);
    //     console.log("obj.num.count", obj1.num.count);
    //     obj1.num.count++;
    //     obj1.user.push("mithu");
    //     console.log("obj1.user", obj1.user);
    // }, 2000);



    // start ref()   
    // const obj2 = ref({count:0});
    // setTimeout( () => {
    //     console.log("obj2", obj2);
    //     console.log("obj2.value", obj2.value);
    //     console.log("obj2.value.count", obj2.value.count);
    //     obj2.value.count++;

    // }, 2000);


    // const obj3 = {count:ref(0)};
    // setTimeout( () => {
    //     console.log("obj3", obj3);
    //     console.log("obj3.count", obj3.count);
    //     console.log("obj3.count.value", obj3.count.value);
    //     obj3.count.value++
    // }, 2000);


    const obj4 = ref({count: ref(0)});

    setTimeout( ()=> {
        console.log("obj4", obj4);
        console.log("obj4.value", obj4.value);
        console.log("obj4.value.count", obj4.value.count);
        obj4.value.count++;
    }, 2000);

</script>

<template>
    <!-- <h1>Addition: {{num.a + num.b}}</h1> -->

    <!-- <h1>Count: {{obj.count}}</h1> -->


    <!-- Deep Reactivity -->
    <!-- <h1>Count: {{obj1.num}}</h1> -->
    <!-- <h1>Count: {{obj1.num.count}}</h1>
    <h1>User: {{obj1.user}}</h1> -->



    <!-- <h1>count: {{ obj2.count }}</h1> -->
    <!-- <h1>count: {{ obj3.count }}</h1> -->
    <!-- <h1>count: {{ obj3.count.value + 5 }}</h1> -->

    <h1>count: {{ obj4.count}}</h1>
</template>

<style scoped></style>