<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Indecision/>
    
  </div>
</template>

<script>
import Indecision from '../src/components/Indecision'

export default {
  name: 'App',
  components: {
    Indecision
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
