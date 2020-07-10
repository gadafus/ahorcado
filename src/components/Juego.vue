<template>
  <div class="container">
    <div class="alert alert-primary" role="alert">
      <h1>Ahorcado</h1>
    </div>
    <div>
      <button v-on:click="elegirPalabra()" type="button" class="btn btn-success">
        <h1>Inicio</h1>
      </button>
    </div>
    

    <div >
      <h1 class="guiones">_</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Juego",
  props: {},

  data() {
    return {
      
    }
  },

  methods: {
        
    }
}

</script>

<style >
.guiones {
  font-size: 500%;
}
</style>