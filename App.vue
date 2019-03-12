<template>
    <enterRoll title="Welcome" label="labeleld :"  placeholder="plaaed" along="horizontal" />
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
@import url(components/styles.css);
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
