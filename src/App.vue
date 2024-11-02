<script setup>
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/Educacion.vue';
// import Experiencia from './components/Experiencia.vue';
// import Habilidades from './components/Habilidades.vue';
// import Intereses from './components/Intereses.vue';
import navBar from './components/navBar.vue';
// import Proyectos from './components/Proyectos.vue';
</script>

<template>
  <header>
    <!-- nav bar -->
    <nav-bar />
    <h1>hola mundillo</h1>
    <!-- datos personales -->
     <DatosPersonales/>
     
  </header>
  <main>
    <section id="educacion">
      <h2>Educación - Cursos</h2>
      <Educacion />
    </section>

    <section id="experiencia">
      <h2>Experiencia</h2>
      <Experiencia />
    </section>

    <section id="proyectos">
      <h2>Proyectos</h2>
      <Proyectos />
    </section>

    <section id="habilidades">
      <h2>Habilidades</h2>
      <Habilidades />
    </section>

    <section id="intereses">
      <h2>Intereses</h2>
      <!-- <Intereses /> -->
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
