<template>
    <div>
        <h2>Coche</h2>
        <!-- Asi se utiliza la variable -->

        <p>Marca: {{ marca }}</p>
        <p>Modelo: {{ modelo }}</p>
        <p>
            Color:

            // Recorriendo sobre la matriz e imprimiendo el índice y el valor de la matriz en un span.
            <span v-for="(color, index) in colors" :key="index">
                {{ index }}: {{ color }}
            </span>
        </p>
        <p> Color:
            // Recorriendo sobre la matriz de colores e imprimiendo el índice y el valor de la matriz en una lista .
            <ul>
            <li v-for="(color, index) in colors" :key="index">
                {{ index }}: {{ color }} -
            </li>
        </ul></p>
        <!-- asi se accede a un array de objetos -->
        <p>Velocidad: {{ velocidad }} km/h</p>
        <p>Potencia: {{ caballos }}</p>
        {{ mensaje.title }} - {{ mensaje.text }}
        <!-- asi se accede a los atributos de un objeto -->
    </div>
</template>

<script>
export default {
    setup() {
        const marca = "Ford";
        const modelo = "Mustang";
        const colors = ["Rojo", "Azul", "Blanco", "Negro"]; // variable de tipo array
        const velocidad = "260";
        const caballos = [240, 280, 320, 400, 480, 520, 826];
        const mensaje = {
            //variable de tipo objeto
            title: "Una verdadera marca",
            text: "Ford Shelby",
        };

        return {
            marca,
            modelo,
            colors,
            velocidad,
            caballos,
            mensaje,
        };
    },
};
</script>

<style scoped></style>
