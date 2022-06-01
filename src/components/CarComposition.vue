<template>
    <h2>Coche - Composition API</h2>
    <!-- Asi se utiliza la variable -->

    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Power: {{ power }}</p>
    <button @click="upPower(20)">+ Power</button>
    <button @click="downPower">- Power</button>

    <!-- Asi se utiliza condiconales v-if con v-for -->
    <!-- <p>Potencias Urbanas menor 320 CV </p>
        <ul>
        <template v-for="(caballo, index) in caballos" :key="index">
            <li v-if="caballo <=320">{{ caballo }}</li>
        </template>
        </ul>
        <p>Potencias Competición mayores 320 CV </p>
        <ul>
        <template v-for="(caballo, index) in caballos" :key="index">
            <li v-if="caballo >320">{{ caballo }}</li>
        </template>
        </ul> -->
    <!-- Así se utiliza condicionales v-else con v-for -->
    <!-- <p>Potencias Urbanas menor 320 CV </p>
        <ul>
        <template v-for="(caballo, index) in caballos" :key="index">
            <li v-if="caballo <=320">{{ caballo }}</li>
        </template>
        </ul> -->
    <!-- Así se utiliza condicionales v-else-if con v-for -->
    <!-- <p>Potencias</p>
        <ul>
        <template v-for="(caballo, index) in caballos" :key="index">
            <li v-if="caballo < 320">Urbano: {{ caballo }}</li>
            <li v-else-if="caballo === 320">Hibrido: {{ caballo }}</li>
            <li v-else>Competición: {{ caballo }}</li>
        </template>
        </ul>

        <p>
            Color: -->

    <!-- // Recorriendo sobre la matriz e imprimiendo el índice y el valor de la matriz en un span. -->
    <!-- <span v-for="(color, index) in colors" :key="index">
                {{ index }}: {{ color }}
            </span>
        </p>
        <p> Color: -->
    <!-- // Recorriendo sobre la matriz de colores e imprimiendo el índice y el valor de la matriz en una lista . -->
    <!-- <ul>
            <li v-for="(color, index) in colors" :key="index">
                {{ index }}: {{ color }} -
            </li>
        </ul></p> -->
    <!-- asi se accede a un array de objetos -->
    <!-- <p>Velocidad: {{ velocidad }} km/h</p>
        <p>Potencia: {{ caballos }}</p>
        {{ mensaje.title }} - {{ mensaje.text }} -->
    <!-- asi se accede a los atributos de un objeto -->
</template>

<script>
import { ref } from "vue";

export default {
    setup() {
        const brand = "Ford";
        const model = "Mustang";
        const colors = ["Rojo", "Azul", "Blanco", "Negro"]; // variable de tipo array
        const speed = "260";
        let power = ref(480);
        const menssaje = {
            //variable de tipo objeto
            title: "Una verdadera marca",
            text: "Ford Shelby",
        };

        const upPower = (newPower) => {
            // console.log("Aumentar potencia");
            power.value = power.value + newPower;
        };

        const downPower = () => {
            // console.log("Disminuir potencia");
            power.value--;
        };

        return {
            brand,
            model,
            colors,
            speed,
            power,
            menssaje,
        };
    },
};
</script>

<style scoped></style>
