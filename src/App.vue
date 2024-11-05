<script setup>
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionC.vue';
import Experiencia from './components/ExperienciaC.vue';
import Habilidades from './components/HabilidadesC.vue';
import Intereses from './components/InteresesC.vue';
import navBar from './components/navBar.vue';
import Proyectos from './components/ProyectosC.vue';
</script>

<template>
  <header>
    <!-- nav bar -->
    <nav-bar />
    <!-- datos personales -->
    <DatosPersonales />

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
      <Intereses />
    </section>
  </main>
</template>

<style scoped>


h2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: xxx-large;
}
section #habilidades{
  margin-bottom: 0 ;
  padding-bottom: 0%;
}
section #intereses{
  margin-top: -10;
  padding-top: 0;
  z-index: 1;
}
</style>
