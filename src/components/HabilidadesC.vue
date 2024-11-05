<script setup>
import img13 from '/src/components/icons/angular.svg';
import img19 from '/src/components/icons/arg.svg';
import img10 from '/src/components/icons/bootstrap.svg';
import img9 from '/src/components/icons/django.svg';
import img20 from '/src/components/icons/eeuu.svg';
import img14 from '/src/components/icons/figma.svg';
import img11 from '/src/components/icons/git.svg';
import img3 from '/src/components/icons/html-css.svg';
import img4 from '/src/components/icons/java.svg';
import img1 from '/src/components/icons/js.svg';
import img12 from '/src/components/icons/microsoft-365.svg';
import img21 from '/src/components/icons/microsoft-centered.svg';
import img16 from '/src/components/icons/mongo.svg';
import img17 from '/src/components/icons/mysql.svg';
import img8 from '/src/components/icons/node.svg';
import img2 from '/src/components/icons/python.svg';
import img6 from '/src/components/icons/react.svg';
import img5 from '/src/components/icons/sql.svg';
import img15 from '/src/components/icons/visualcode.svg';
import img7 from '/src/components/icons/vue.svg';
import img18 from '/src/components/icons/wordpress.svg';

import { ref } from 'vue';
const habilidades = ref([
  {
    id: 1, nombre: 'Lenguajes de Programación', habilidades: [
      { id: 1, nombre: 'JavaScript', nivel: 'Avanzado', icono: img1 },
      { id: 2, nombre: 'Python', nivel: 'Intermedio', icono: img2 },
      { id: 3, nombre: 'HTML/CSS', nivel: 'Avanzado', icono: img3 },
      { id: 4, nombre: 'Java', nivel: 'Avanzado', icono: img4 },
      { id: 5, nombre: 'SQL', nivel: 'Avanzado', icono: img5 }
    ]
  },
  {
    id: 2, nombre: 'Frameworks y Librerías', habilidades: [
      { id: 1, nombre: 'React.js', nivel: 'Intermedio', icono: img6 },
      { id: 2, nombre: 'Vue.js', nivel: 'Intermedio', icono: img7 },
      { id: 3, nombre: 'Node.js', nivel: 'Intermedio', icono: img8 },
      { id: 4, nombre: 'Django', nivel: 'Basico', icono: img9 },
      { id: 5, nombre: 'Bootstrap', nivel: 'Avanzado', icono: img10 },
      { id: 6, nombre: 'Angular', nivel: 'Basico', icono: img13 }
    ]
  },
  {
    id: 3, nombre: 'Herramientas y Software', habilidades: [
      { id: 1, nombre: 'Git', nivel: 'Intermedio', icono: img11 },
      { id: 2, nombre: 'Microsoft-365', nivel: 'Avanzado', icono: img12 },
      { id: 3, nombre: 'CRM Microsoft', nivel: 'Avanzado', icono: img21 },
      { id: 4, nombre: 'Figma', nivel: 'Avanzado', icono: img14 },
      { id: 5, nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: img15 },
      { id: 6, nombre: 'WordPress', nivel: 'Basico', icono: img18 }
    ]
  },
  {
    id: 4, nombre: 'Bases de Datos', habilidades: [
      { id: 1, nombre: 'MongoDB', nivel: 'Basico', icono: img16 },
      { id: 2, nombre: 'MySQL', nivel: 'Intermedio', icono: img17 }
    ]
  },
  {
    id: 5, nombre: 'Idiomas', habilidades: [
      { id: 1, nombre: 'Español', nivel: 'Nativo', icono: img19 },
      { id: 2, nombre: 'Inglés', nivel: 'Intermedio (B2)', icono: img20 }
    ]
  }
])
</script>

<template>
  <div class="skills-contenedor">
    <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
      <h3>{{ habilidad.nombre }}</h3>
      <ul class="skills">
        <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
          <img :src="habilidad.icono" :alt="habilidad.nombre">
          <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
        </li>
      </ul>
    </div>
  </div>

</template>

<style scoped>

.skills-contenedor {
  padding: 2rem;
  border-radius: 1rem 1rem 0 0;
  position: relative;
  background-image: linear-gradient(to bottom, #86377b 20%, #27273c 100%);
  margin-bottom: 0;
  margin: 0 auto;
}

.skills-categoria {
  margin-bottom: 20px;
}

.skills-categoria h3 {
  margin-bottom: 10px;
  font-size: 1.5em;
  font-weight: bold;
  color: #000;
  text-align: center;
}

.skills {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  gap: 20px;
}

.skill {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  background-color: rgba(241, 245, 243, 0.856);
  padding: 0.3em;
  border-radius: 8px;
  box-shadow: 0px 4px 12px rgba(94, 96, 96, 0.963);
  flex: 1 1 200px;
  max-width: 250px;
}

.skill:hover {
  background-color: var(--vt-c-purple-soft);
}

.skill img {
  width: 35px;
  height: 35px;
}

.skill span {
  font-size: 1em;
  color: #040404;
}

.skill span:hover {
  font-size: 1.3em;
  transition: 2s ease;
  color: var(--vt-c-white);
}

@media (max-width: 768px) {
  .skills-categoria h3 {
    justify-content: center;
  }

  .skill {
    justify-content: center;
  }
}
</style>
