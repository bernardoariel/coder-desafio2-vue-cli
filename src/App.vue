<template>
  <div id="app">
    <ContenedorComponent />
  </div>
</template>

<script>

import ContenedorComponent from './components/ContenedorComponent'

export default {
  name: 'App',
  components: {
    ContenedorComponent
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
