<template>
  <div id="enter-roll-box">
    <div id=welcome-text>WELCOME
    </div>
    <div id="inputroll">
      <div id="input-roll-label"></div>
      <input id="input-roll-box" />
    </div>
    <button id="submit">Next</button>
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #input-roll-box
  {
    display: grid;
    width:100%;
    height: 100%;
    align-content: center;
  }
  #welcome-text
  {
    align-content: center;
    justify-content: center;
    font-family: sans-serif;
    font-size:200%
  }
</style>
