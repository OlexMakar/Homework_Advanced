<template>
  <div id="app">    
    <MyCalc/>
  </div>
</template>

<script>
import MyCalc from "./components/MyCalc";


export default {
  name: 'App',
  components: {
    MyCalc    
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
  margin-top: 63px;
}
</style>
