<template>

  <div id="enter-roll-box">
    <div id=welcome-text>Is it your first visit?
    </div>
    <hr>
    <br><br>
    <div class="fieldsContainer">
      <div id="inputroll">
        <br><labeled-input class=".input-and-label" placeholder="Name" label="Enter Name" along="vertical" ></labeled-input>
      
      </div>
      <br>
      <div id="securityQuestion">
        <br><labeled-input class=".input-and-label" placeholder="Secret" label="Question Comes" along="vertical" ></labeled-input>
      
      </div>
    </div>
    <br><br>
    <button id="verify" class="surface_2 interactive"><i class="fab fa-google fa-2x"></i>&nbsp;<span>Verify via Google</span></button>
  </div>
</template>
<script>
import labeledInput from "./labeled-input";
export default {
  components:{
    labeledInput
  }
}
</script>
<style scoped>
    @import url('https://use.fontawesome.com/releases/v5.7.2/css/all.css');
    @import url('https://fonts.googleapis.com/css?family=Aclonica');
  #enter-roll-box {
    width: 100%;
    padding: 10px;
    border: 1px solid #e0cdcd;
    border-radius: 5px;
    box-shadow: 0px 0px 6px 1px #c1baba;

  }
  hr{
    border: 0.5px solid #cabebe;

      width: 80%;
  }
  .label
  {
      color: #155a6b;
  }
  div
  {
      font-family: 'Aclonica', sans-serif;

  }
  #welcome-text
  {
      color: #00a4d3;
      font-family: 'Aclonica', sans-serif;
      font-size: 35px;
      text-align: center;
  }

  input {
    
    border-radius: 5px;
    padding: 10px;
    border: 1px solid #0b758e;
    height: 20px;
    width: calc( 100% - 40px);
  }
  input:focus
  {
      outline-width: 0px;
  }
  button:focus
  {
      outline-width: 0px;
  }
  #verify
  {
    background:transparent;
    padding: 15px;
    width: 220px;
    color: #16b92c;
    display: block;
    margin:auto;
   

  }
  

</style>
