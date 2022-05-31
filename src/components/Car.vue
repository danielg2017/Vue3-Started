<template>
    <div>
        <h2>Coche</h2>
        <!-- Asi se utiliza la variable con Options API, vue2  y tambien con composition Api, vue3-->
        <p>Marca: {{ marca }}</p>
        <p>Modelo: {{ modelo }}</p>
        <p>Color: {{ color[0] }}</p>
        asi se accede a un array de objetos
        <p>Velocidad: {{ velocidad }} km/h</p>
        <p>Potencia: {{ caballos }}</p>
        {{ mensaje.title }} - {{ mensaje.text }}
        <!-- asi se accede a los atributos de un objeto -->
    </div>
</template>

<script>
export default {
    // // Asi se declaran las variables con Options API, vue2
    // data() {
    //     return {
    //         marca: "Ford",
    //         modelo: "Mustang",
    //         color: ["Rojo", "Azul", "Blanco", "Negro"], // variable de tipo array
    //         velocidad: 240,
    //         caballos: "500",
    //         mensaje: {
    //             //variable de tipo objeto
    //             title: "Una verdadera marca",
    //             text: "Ford Shelby",
    //         },
    //     };
    // },
    // // Asi se declaran las variables con Options API, vue2

    setup() {
        const marca = "Ford";
        const modelo = "Mustang";
        const color = ["Rojo", "Azul", "Blanco", "Negro"]; // variable de tipo array
        const velocidad = "260";
        const caballos = "520";
        const mensaje = {
            //variable de tipo objeto
            title: "Una verdadera marca",
            text: "Ford Shelby",
        };

        return {
            marca,
            modelo,
            color,
            velocidad,
            caballos,
            mensaje,
        };
    },
};
</script>

<style scoped></style>
