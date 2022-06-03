<template>
    <h2>Coche - Composition API</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <!-- proceso donde podemos trabajar la funcion en este componente antes de pasar -->
    <!-- <button @click="testPower">Aumentar potencia</button> -->
    <!-- proceso para pasar la funcion de forma directa -->
    <button @click="upPower">Aumentar potencia</button>
    <button @click="downPower">Disminuir Potencia</button>
</template>

<script>
export default {
    props: {
        power: {
            type: Number,
            default: 280,
        },
        upPower: {
            type: Function,
            default: () => {},
        },
        downPower: {
            type: Function,
            default: () => {},
        },
    },

    setup(props) {
        const brand = "Ford";
        const model = "Mustang";

        // crear un funcion y exportarla para utilizar en el mismo componente
        // console.log(props);

        // const testPower = () => {
        //     props.upPower();
        // };

        return {
            brand,
            model,
            // testPower,
        };
    },
};
</script>

<style scoped></style>
