<script setup>

import { ref } from 'vue';
const titulo = 'Desarrollador Full Stack';
const fecha = 'Desde Enero 2022 / Julio 2024';
const experiencias = ref([
    { id: 1, src: "", parrafo: '' },
    { id: 2, src: "", parrafo: '' },
    { id: 3, src: "", parrafo: '' },
    { id: 4, src: "", parrafo: '' },
]);
</script>
<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>

        </ul>
    </div>
</template>
<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>