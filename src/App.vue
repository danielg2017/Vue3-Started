<template>
    <div>
        <h1>Vue 3 Js</h1>
        <CarOption />
        <hr />
        <CarComposition />
    </div>
</template>

<script>
import CarComposition from "./components/CarComposition.vue";
import CarOption from "./components/CarOption.vue";

export default {
    components: {
        CarComposition,
        CarOption,
    },
};
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>
