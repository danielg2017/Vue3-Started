<template>
    <div>
        <h1>Vue 3 Js</h1>
        <Car :power="power" />
    </div>
</template>

<script>
import Car from "./components/Car.vue";

export default {
    components: {
        Car,
    },

    setup() {
        let power = 580;
        return {
            power,
        };
    },
};
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>
