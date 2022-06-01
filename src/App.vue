<template>
    <div>
        <h1>Vue 3 Js</h1>
        <Car :power="power" :upPower="upPower" />
    </div>
</template>

<script>
import { ref } from "vue"; // importar la funcion ref de vue para crear una referencia
import Car from "./components/Car.vue";

export default {
    components: {
        Car,
    },

    setup() {
        let power = ref(580); // crear una referencia para el valor de la potencia

        const upPower = () => {
            // crear una funcion para aumentar la potencia
            power.value += 10; // aumentar la potencia
            console.log("aumentar power...");
        };

        return {
            power,
            upPower,
        };
    },
};
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>
