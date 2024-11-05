<script setup>
import it from '/src/assets/itconsultant logo.jpg';
import zn from '/src/assets/zennonbi.jpg';
import escudo from '/src/assets/elescudo.jpg';

import { ref } from 'vue';
const titulo = 'Analista Tecnico Funcional, especializado en CRM Dinamics 365.';
const fecha = 'Desde 2022 / Actualidad';
const experiencias = ref([
  { id: 1, src: it, parrafo: 'Zennon BI. Personalmente me destaco por mi trabajo como desarrolladora y analista funcional. Utilizando herramientas aprendidas en mi carrera como Técnica en Administración y tecnologías de desarrollo como Html, CSS, JavaScript, C# y .NET con herramientas como Postman, GitHub y principalmente CRM de Microsoft Dynamics 365. Actualmente dedico el 100% de mi tiempo laboral en el cliente Banco Provincia Microcréditos. Zennon Bi es una consultora Partner Microsoft que ofrece diversos servicios, productos y aplicaciones integradas a través de las herramientas de Microsoft Dynamics 365 y extensiones que usan Microsoft Azure, SharePoint y Office 365.' },
  { id: 2, src: zn, parrafo: 'IT Consultant. Actualmente trabajo de forma exclusiva con el cliente Banco Provincia Microcréditos, donde me destaco por mi trabajo como desarrolladora y analista funcional. Utilizo a lo largo de mi jornada las herramientas aprendidas en mi carrera como Técnica en Administración y tecnologías de desarrollo como HTML, CSS, JavaScript, C# y.NET con herramientas como Postman, GitHub y principalmente CRM de Microsoft Dynamics 365.' },
  { id: 4, src: escudo, parrafo: 'Escudo Materiales. Administración de facturas de compra y venta.Actualización de precios, productos y compras dentro del sistema. Administración y manejo de las necesidades del personal.' },
]);
</script>
<template>
  <div class="card">
    <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
    <p class="fecha">{{ fecha }}</p>
    <ul class="listado">
      <li class="item" v-for="experencia in experiencias" :key="experencia.id">
        <img v-if="experencia.src" class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
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
  background-color:var(--vt-c-soft-gray);
  border-radius: 15px;
}

.titulo {
  font-size: 2rem;
  color: var(--vt-c-gold);
}

.fecha {
  font-size: 1.5rem;
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

.imagen-svg{
  width: 10%;
}
</style>
