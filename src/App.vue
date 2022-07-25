<template>
  <div class="logo">
      <img alt="Vue logo" src="./assets/logo.png" width="250" height="150">
  </div>
  <Conteudo msg="Centro de Treinamento UBT"/>

</template>

<script>
import Conteudo from './components/Conteudo.vue'

export default {
  name: 'App',
  components: {
    Conteudo
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
    }

</style>
