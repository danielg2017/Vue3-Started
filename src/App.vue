<template>
    <div>
        <h1>Vue 3 Js</h1>
        <Car :power="power" :upPower="upPower" :downPower="downPower" />
        <!-- utilizando emmit para emitir eventos en la funcion disminuir potencia -->
        <!-- <Car :power="power" :upPower="upPower" @downPower="downPower" /> -->
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
            power.value += 10; // aumentar la potencia en 10
            console.log("aumentar power...");
        };

        const downPower = () => {
            // crear una funcion para disminuir la potencia
            power.value -= 10; // disminuir la potencia en 10
            console.log("disminuir power...");
        };

        return {
            power,
            upPower,
            downPower,
        };
    },
};
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>
