<template>
  <div v-bind:class="restaVida()">{{vidas}}</div>
</template>

<script>
import bus from "../bus";

export default {
    name: "Vidas",
    props: {
        
    },

  data() {
    return {
      vidas: 5
    };
  },

  methods: {
    restaVidas: function() {
      bus.$on('falloLetra', this.vidas = this.vidas -1);
      return this.vidas;
    }
  } 
  /* created() {
    bus.$on("falloLetra", restaVida => {
      this.vidas = this.vidas - 1;
    });
  } */
};
</script>

<style>
</style>