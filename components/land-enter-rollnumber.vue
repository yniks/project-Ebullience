<template>
  <div id="main-roll-box" class="surface_1">
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
import ebulButton from "./ebul-button"
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
    box-sizing: border-box;
    align-content: center;
    justify-items: center;
    grid-template-columns: 1fr;
    grid-template-rows: 1.5fr 1.6fr 1fr;
  }
  #label-input-container,.input-and-label
  {
    width:100%;
  }
  #welcome-text
  {
    padding:2vw;
    font-size:3em;
    color: #00a4d3;
  }
  #submit-button
  {
    justify-self: end;
    padding: 12px;
  }

</style>
