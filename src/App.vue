<script setup>
import navBar from './components/navBar.vue';
</script>

<template>
  <header>
    <!-- nav bar -->
    <nav-bar />
    <h1>hola mundillo</h1>
    <!-- datos personales -->
  </header>
  <main>
    <!-- secciones -->
  </main>
  <footer>
    <a href="#top">Inicio</a>
    <p> Portafolio web - tutorial UTN FRSR</p>
  </footer>
</template>

<style scoped>
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
}
</style>
