<script setup>
import { ref } from 'vue';

const intereses = ref([
  'Fotografia:',
  ' Me encanta el mundo de la fotografia.En el año 2022 logre comprar mi primera camara de fotos Nikon luego de mucho esfuerzo. En el año 2023 realice un curso de fotografia para perfeccionarme aun más.Mi tipo de fotografia favorito es el deportivo.',
  'Ceramica:',
  ' En el 2023 descubri el mundo de la ceramica, me apasiono el trabajar con las manos y potenciar la creatividad en cada pieza. Además, el proceso de hacer ceramica te ayuda a trabajar la frustracion, la paciencia y el detalle.',
  'Cocina:',
  ' Disfruto mucho cocinar y probar recetas nuevas, soy de la generacion que crecio mirando Utilisima y el Gourmet. Mi comida preferida son las pastas rellenas con crema de hongos.',
  'Deporte:',
  ' Me apasiona el automovilismo y todas sus variantes. Tuve un auto para correr picadas, fue un hermoso proyecto que tuvimos en conjunto con mi novio. Además, los domingos son de carreras de F1, de motocross o la categoria zonal de donde vivo.'
]);
</script>

<template>
  <div class="intereses-contenedor">
    <ul class="contenedor-lista">
      <h2>Intereses</h2>
      <li class="item" v-for="interes in intereses" :key="interes">
        {{ interes }}
      </li>
    </ul>
    <div class="waveWrapper waveAnimation">
      <div class="waveWrapperInner bgTop">
        <div class="wave waveTop" style="background-image: url('http://front-end-noobs.com/jecko/img/wave-top.png')">
        </div>
      </div>
      <div class="waveWrapperInner bgMiddle">
        <div class="wave waveMiddle" style="background-image: url('http://front-end-noobs.com/jecko/img/wave-mid.png')">
        </div>
      </div>
      <div class="waveWrapperInner bgBottom">
        <div class="wave waveBottom" style="background-image: url('http://front-end-noobs.com/jecko/img/wave-bot.png')">
        </div>
      </div>
    </div>
    <footer>
      <a href="#top">Inicio</a>
      <p> Portafolio web - Cecilia Olejarczyk 2024</p>
    </footer>
  </div>
</template>

<style scoped>
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
  z-index: 2000;
  margin-bottom: 0%;
}

footer a,
p {
  color: black;
  font-weight: 1000;
}

body,
html,
h2 {
  overflow-x: hidden;
  text-align: center;
}

.intereses-contenedor {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  margin: -1px auto;
  max-width: 100%;
  padding: 1rem;
  overflow: hidden;
}

.contenedor-lista {
  list-style-type: none;
  padding: 1rem;
  margin-bottom: 0.5rem;
  color: var(--vt-c-white);
  font-size: 1.4rem;
  text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
  z-index: 1000;
  justify-content: center;
}

.item {
  margin-bottom: 1rem;
}

.waveWrapper {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  margin: auto;
}

.waveWrapperInner {
  position: absolute;
  width: 100%;
  height: 100%;
  bottom: -1px;
  background-image: linear-gradient(to top, #86377b 20%, #27273c 90%);
}

.bgTop {
  z-index: 15;
  opacity: 0.5;
}

.bgMiddle {
  z-index: 10;
  opacity: 0.75;
}

.bgBottom {
  z-index: 5;
}

.wave {
  position: absolute;
  left: 0;
  width: 200%;
  height: 100%;
  background-repeat: repeat-x;
  background-position: 0 bottom;
  transform-origin: center bottom;
}

.waveTop {
  background-size: 50% 100px;
}

.waveMiddle {
  background-size: 50% 120px;
}

.waveBottom {
  background-size: 50% 100px;
}

.waveAnimation .waveTop,
.waveAnimation .waveMiddle,
.waveAnimation .waveBottom {
  animation: move_wave 10s linear infinite;
}

@keyframes move_wave {
  0% {
    transform: translateX(0) translateZ(0) scaleY(1);
  }

  100% {
    transform: translateX(-25%) translateZ(0) scaleY(1);
  }
}
</style>
