<template>
  <input type="text" v-model="letras" v-on:keyup="teclaPulsada($event)">
</template>

<script>
import bus from '../bus'

export default {
    data() {
        return {
            letras: '',
        }
    },

    methods: {

        teclaPulsada(event){
            bus.$emit('newKey', event.key);
            console.log(event);
        }

    }

}
</script>

<style>

</style>