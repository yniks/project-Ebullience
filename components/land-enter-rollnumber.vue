<template>
  <div id="main-roll-box">
    <div id=welcome-text>Welcome</div>
    <div id="label-input-container">
      <labeled-input class=".input-and-label" placeholder="Roll Number" label="Enter Roll Number :" along="vertical" ></labeled-input>
      </div>
    <div id="submit-button">
      <ebul-button>Next</ebul-button>
    </div>
  </div>
</template>
<script>
import labeledInput from "./labeled-input";
import ebulButton from "./button"
export default {
  components:{
    labeledInput,
    ebulButton
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Aclonica);
  #main-roll-box
  {
    display: grid;
    width:100%;
    height: 100%;
    text-align: center;
    align-content: center;
    padding: 20px;
    grid-template-rows: 1.5fr 1.6fr 1fr;
    background: rgba(255,255,255,0.5);
    box-shadow:0px 0px 9px rgba(61,5,27,0.54);
    border: 0px;
    border-radius: 15px;
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

</style>
