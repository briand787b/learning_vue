<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>Hello World</div>
    <div v-if="truthy">Conditionally Shown</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  data: {
    truthy: true
  },
  components: {
    HelloWorld,
    truthy: true
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
