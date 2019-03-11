<template>
  <div id="app">
    <img src="./assets/logo.png">
    <enterRoll/>
  </div>
</template>

<script>
import enterRoll from './components/land-enter-rollnumber'

export default {
  name: 'App',
  components: {
    enterRoll
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
