<template>
    <div>
        <h2>Coche - Option API</h2>
        <!-- Asi se utiliza la variable -->

        <p>Marca: {{ brand }}</p>
        <p>Modelo: {{ model }}</p>
        <p>Potencia: {{ power }}</p>
    </div>
    <button @click="powerUp(20)">Disminuir</button>
    <button @click="powerDown">Aumentar</button>
</template>

<script>
export default {
    data() {
        return {
            brand: "Ford",
            model: "Mustang",
            power: 480,
            colors: ["Rojo", "Azul", "Blanco", "Negro"], // variable de tipo array
            velocidad: 0,
            mensaje: {
                //variable de tipo objeto
                title: "Una verdadera marca",
                text: "Ford Shelby",
            },
        };
    },
    methods: {
        powerUp(newPower) {
            console.log("Aumentar potencia");
            this.power = this.power + newPower;
        },
        powerDown() {
            console.log("Disminuir potencia");
            this.power--;
        },
    },
};
</script>

<style scoped></style>
