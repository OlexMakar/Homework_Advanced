<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <converter/>
  </div>
</template>

<script>
import converter from './components/converter.vue'

export default {
  name: 'App',
  components: {
    converter
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
