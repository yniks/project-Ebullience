<template>
  <div id="enter-roll-box">
    <div id=welcome-text>Welcome
    </div>
    <div id="label-input-container">
      <labeled-input class=".input-and-label" placeholder="Roll Number" label="Enter Roll Number :" along="vertical" ></labeled-input>
      <labeled-input class=".input-and-label" placeholder="Secrete" label="Enter Secrete:" along="vertical" type="password"></labeled-input>
    </div>
    <div id="submit-button">
      <button id=button-submit class="surface_2 interactive">Next</button>
    </div>
  </div>
</template>
<script>
import labeledInput from "./labeled-input";
export default {
  name: 'HelloWorld',
  components:{
    labeledInput
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Aclonica);
  #enter-roll-box
  {
    display: grid;
    width:90%;
    height: 100%;
    text-align: center;
    align-content: center;
    padding: 20px;
    grid-template-rows: 1.5fr 2fr 1fr;
    background: rgba(255,255,255,0.5);
    box-shadow:0px 0px 9px rgba(61,5,27,0.54);
    border: 0px;
    border-radius: 15px;
  }
  #input-roll-label
  {
    text-align: left;
    padding-bottom: 12px;
    color: #115555;
    font-size: 1.2em
  }
  #input-roll
  {
    height: 3em;
    opacity: 0.75;
  }
  #label-input-container
  {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      padding:12px;
  }
  .input-and-label
  {
    width:100%;
  }
  #welcome-text
  {
    align-content: center;
    justify-content: center;
    padding:2vw;
    font-size:3em;
    color: #00a4d3;
  }
  #submit-button
  {
    text-align: right;
    padding: 12px;
  }
  #button-submit
  {
    height:2.7em;
    min-width: 5em;
    width: 7vw;
  }

</style>
