<script setup>
import Experiencia from './components/Experiencia.vue';
import Habilidades from './components/Habilidades.vue';
import Intereses from './components/Intereses.vue';
import navBar from './components/navBar.vue';
import Proyectos from './components/Proyectos.vue';
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
    <!--el estilo css de section se encuentra en base.css-->
    <section id="educacion">
      <h2>Educación - Cursos</h2>
      <!--Componente Educación-->
      <Educacion />
    </section>
    <section id="experiencia">
      <h2>Experiencia</h2>
      <!--Componente Experiencia-->
      <Experiencia />
    </section>
    <section id="proyectos">
      <h2>Proyectos</h2>
      <!--Componente Proyectos-->
      <Proyectos/>
    </section>
    <section id="habilidades">
      <!--Componente Habilidades-->
      <h2>Habilidades</h2>
      <Habilidades />
    </section>
    <section id="intereses">
      <!--Componente Intereses-->
      <h2>Intereses</h2>
      <Intereses />
    </section>
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
