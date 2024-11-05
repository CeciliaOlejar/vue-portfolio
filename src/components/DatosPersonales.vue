<script setup>
import linkedin from '/src/assets/linkedin_icon.svg';
import instagram from '/src/assets/instagram_icon.svg';
import github from '/src/assets/github_icon.svg';
import cv from '/src/assets/cv_resume_icon.svg';
import wpp from '/src/assets/whatsapp-icon.svg';

const title = 'Cecilia Olejarczyk';
const descripcion = 'Técnico Universitario en Programación - UTN';
const presentacion = 'Hola! Bienvenida/o a mi portafolio de proyectos.';
const presentacion2 = 'Desde hace 3 años que vengo realizando diversas capacitaciones sobre desarrollo web y lenguajes de programación como JavaScript, Python, Java y C# con.NET.';
const presentacion3 = 'Actualmente me encuentro desde dos años trabajando para Banco Provincia Microcréditos como desarrolladora especializada en CRM';
const redesSociales = [
  { id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/' },
  { id: 2, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/' },
  { id: 3, name: 'github', src: github, url: '' },
  { id: 4, name: 'curriculum', src: cv, url: '' },
  { id: 5, name: 'wpp', src: wpp, url: ''},
];
const residencia = 'Santa Clara del Mar, Buenos Aires, Argentina';
</script>

<template>
  <section class="datos-personales">
    <div class="bg"></div>
    <div class="bg bg2"></div>
    <div class="bg bg3"></div>
    <div class="content">
      <div class="card">
        <div class="nomfont">{{ title }}</div>
        <h1>{{ descripcion }}</h1>
        <h3>{{ presentacion }}</h3>
        <h4>{{ presentacion2 }}</h4>
        <p>{{ presentacion3 }}</p>
        <ul class="container-lista">
          <li v-for="red in redesSociales" :key="red.id">
            <a :href="red.url" target="_blank" rel="noopener noreferrer">
              <img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name">
            </a>
          </li>
        </ul>
        <h3>{{ residencia }}</h3>
      </div>
    </div>
  </section>
</template>

<style>
.nomfont {
  font-family: "Playwrite GB S", cursive;
  font-optical-sizing: auto;
  font-size: xxx-large;
  font-weight: auto;
  font-style: italic;
}
.card {
  position: relative;
  color: var(--vt-c-white);
  border-radius: 1.5rem;
  padding: 1rem;
  margin: 2rem;
  text-align: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5);
  width: 100%;
  overflow: hidden;
}

.card::before,
.card::after {
  content: '';
  position: absolute;
  top: 0;
  left: -50%;
  right: -50%;
  bottom: 0;
  z-index: -1;
  opacity: 0.5;
  background-image: linear-gradient(-60deg, var(--vt-c-gold) 33.33%, var(--vt-c-pink-accent) 33.33%, var(--vt-c-pink-accent) 66.67%, var(--vt-c-purple) 66.67%);
  animation: slide 6s ease-in-out infinite alternate;
}

.card::after {
  animation-direction: alternate-reverse;
  animation-duration: 4s;
}

@keyframes slide {
  0% {
    transform: translateX(-25%);
  }

  100% {
    transform: translateX(25%);
  }
}

h1,
h2,
h3,
h4,
p {
  margin: 5px 0;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 10px 0;
}

.icon-redsocial {
  align-items: center;
  background-color: var(--vt-c-white);
  border-radius: 50%;
  padding: 5px;
  margin: 5px;
  transition: background-color 0.3s, transform 0.3s;
  box-shadow: 0 0 8px rgba(95, 124, 205, 0.5);
}

.icon-redsocial:hover {
  background-color: var(--vt-c-purple);
  transform: scale(1.1);
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.7);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}
</style>

