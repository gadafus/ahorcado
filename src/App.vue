<template>
  <div id="app">
    <Juego/>
    <Palabra palabra="palabra"/>
    <Letras/>
    <Vidas/>
  </div>
</template>

<script>
import Juego  from './components/Juego.vue';
import Palabra from './components/Palabra.vue';
import Letras from './components/Letras.vue';
import Vidas from './components/Vidas.vue'
export default {
  name: 'App',
  components: {
    Juego,
    Palabra,
    Letras,
    Vidas
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
