<template>
  <nav class="navbar">
    <div class="navbar-header">
      <button class="hamburger" @click="toggleMenu">
        ☰
      </button>
    </div>
    <div class="navbar-menu" :class="{ 'is-active': menuAbierto }">
      <ul class="nav-list">
        <li v-for="nav in navegacion" :key="nav.id" class="nav-item">
          <a :href="nav.enlace" @click="closeMenu">{{ nav.nombre }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';
const menuAbierto = ref(false);

const toggleMenu = () => {
  menuAbierto.value = !menuAbierto.value;
};

const closeMenu = () => {
  menuAbierto.value = false;
};

const navegacion = ref([
  { id: 1, nombre: 'Educación', enlace: '#educacion' },
  { id: 2, nombre: 'Experiencia', enlace: '#experiencia' },
  { id: 3, nombre: 'Proyectos', enlace: '#proyectos' },
  { id: 4, nombre: 'Habilidades', enlace: '#habilidades' },
  { id: 5, nombre: 'Intereses', enlace: '#intereses' }
  // { id: 6, nombre: 'Contacto', enlace: '#Contacto' }

]);
</script>

<style scoped>
.navbar {
  background-color: var(--vt-c-purple);
  border-color: #fff;
  color: #fff;
  padding: 0.5rem 1rem;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1;
}
.hamburger {
  background: none;
  border: none;
  color: #fff;
  font-size: 1.5rem;
  cursor: pointer;
  display: none;
}

.navbar-menu {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.nav-list {
  display: flex;
  flex-direction: row;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-item {
  margin-right: 1rem;
}

.nav-item a {
  color: #fff;
  text-decoration: none;
  padding: 0.5rem;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.nav-item a:hover {
  background-color:gold;
}

@media (max-width: 768px) {
  .hamburger {
    display: block;
  }

  .navbar-menu {
    position: fixed;
    top: 3rem;
    left: 0%;
    width: auto;
    height: auto;
    background-color: var(--vt-c-purple);
    display: none;
    flex-direction: column;
    padding: 3rem 2rem;
    box-shadow: 2px 0 10px rgba(0, 0, 0, 0.4);
    z-index: 2;
    font-size: large;
  }

  .navbar-menu.is-active {
    display: flex;
  }

  .nav-list {
    flex-direction: column;
  }

  .nav-item {
    margin-bottom: 1rem;
  }

  .nav-item:last-child {
    margin-bottom: 0;
  }
}
</style>
