<script setup>
import { ref } from 'vue';
import escudo from '/src/assets/elescudo.jpg';
import rosadita from '/src/assets/la Rosadita.png';
import prome from '/src/assets/provincia-microcreditos.png';
var misProyectos = ref([]);
misProyectos.value = ([
  {
    id: 1,
    src: escudo,
    titulo: "El Escudo Materiales",
    descripcion: `Corralon de Materiales.
    Diseño de pagina web con
    construccion de identidad de marca, logo y paleta de colores.`,
    projectoLink: "https://elescudomaterialesmio.netlify.app/",
    githubLink: "https://github.com/CeciliaOlejar/ElEscudoMateriales"
  },
  {
    id: 2,
    src: rosadita,
    titulo: "La Rosadita",
    descripcion: `Cabañas para alquilar en Camet Norte.
    Diseño de pagina web con
    construccion de identidad de marca, logo y paleta de colores.`,
    projectoLink: "http://www.larosadita.com/",
    githubLink: "https://github.com/CeciliaOlejar/LaRosadita"
  },
  {
    id: 3,
    src: prome,
    titulo: "Desarrolladora CRM",
    descripcion: "Microcréditos del Banco Provincia a travez de la consultoraIT Consultant.",
    projectoLink: "https://provinciamicrocreditos.com.ar/",
  },

]);
</script>
<template>
  <div class="galeria">
    <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
      <img :src="proyecto.src" :alt="proyecto.titlulo">
      <div class="proyecto-info">
        <h3>{{ proyecto.titulo }}</h3>
        <p>{{ proyecto.descripcion }}</p>
        <div class="proyecto-links">
          <a :href="proyecto.projectoLink" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver
            Proyecto</a>
          <a :href="proyecto.githubLink" class="github-link" target="_blank" rel="noopener noreferrer">Ver
            Código en GitHub</a>
        </div>
      </div>
    </li>
  </div>
</template>

<style scoped>
.galeria {
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px;
  justify-content: center;
  background: linear-gradient(70deg, #ffb300, #6a1b9a, #d81b60, #ffb300);
  background-size: 400% 400%;
  animation: gradient 5s ease infinite;
  border-radius: 1.5rem;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}

.proyecto {
  display: flex;
  flex-direction: column;
  border: 2px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  background-color: #f9f9f9;
  flex: 1 1 300px;
  height: auto;
}

.proyecto img {
  width: auto;
  height: 8rem;
  margin: auto;
  margin-top: 1rem;
  object-fit: cover;
}

.proyecto-info {
  padding: 1.5rem;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.proyecto-info h3 {
  margin: 10px 0;
  font-size: 1.3em;
  color: #333;
}

.proyecto-info p {
  margin: 10px 0;
  font-size: 1em;
  color: #666;
  height: auto;
  margin-bottom: 2rem;
}

.proyecto-links {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: auto;
}

.proyecto-links .btn-ver-mas,
.proyecto-links .github-link {
  background-color: #007BFF;
  color: #fff;
  padding: 10px 15px;
  border-radius: 5px;
  text-decoration: none;
  transition: background-color 0.3s;
  text-align: center;
  flex: 1;
}

.proyecto-links .btn-ver-mas:hover {
  background-color: #0056b3;
}

.proyecto-links .github-link {
  background-color: #333;
  color: #fff;
}

.proyecto-links .github-link:hover {
  background-color: #444;
}

</style>
