<template>
    <h2>Coche - Composition API</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
</template>

<script>
export default {
    props: {
        power: {
            type: Number,
            default: 280,
        },
    },
    setup() {
        const brand = "Ford";
        const model = "Mustang";

        return {
            brand,
            model,
        };
    },
};
</script>

<style scoped></style>
