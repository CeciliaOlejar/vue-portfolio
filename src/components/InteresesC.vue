<script setup>
import { ref } from 'vue';
const intereses = ref([
  "interes1",
  "interes2",
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
footer a,p{
  color: black;
  font-weight: 1000;
}

body,
html {
  overflow-x: hidden;
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
  color: var(--vt-c-white-soft);
  font-size: 1.4rem;
  text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
  z-index: 10;
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
  margin:auto;
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
