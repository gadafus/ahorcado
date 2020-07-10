<template>
  <div>
    <div>
      <span v-for="(letra, index) in letras" v-bind:key="index">{{letra.visible?letra.letra: " _ "}}</span>
    </div>
  </div>
</template>

<script>
import bus from "../bus";
export default {
  name: "Palabra",
  props: {
    palabra: String
  },

  data() {
    return {
      letras: []
    };
  },

  methods: {
    /* elegirPalabra: function() {
      this.rand = (Math.random() * 10).toFixed(0);
      this.palabra = this.palabras[this.rand].toUpperCase();
      console.log(this.palabra);
    } */
  },

  created() {
    this.letras = this.palabra.split("").map(i => {
      return { letra: i, visible: false };
    });
    console.log(this.letras);

    bus.$on("newKey", letra => {
      console.log(letra);
      if (this.palabra.includes(letra)) {
        this.letras.forEach(element => {
          if (element.letra == letra) {
            element.visible = true;
          }
        });
      }else {
          bus.$emit('falloLetra', letra)
      }
    });
  }
};
</script>

<style>
</style>