<template>

  <div id="enter-roll-box">
    <div id=welcome-text>Is it your first visit?
    </div>
    <hr>
    <br><br>
    <div class="fieldsContainer">
      <div id="inputroll">
        <div class="label" id="roll-label">Your Name</div>
        <br><input id="input-roll-box" placeholder="Name"/>
      </div>
      <br>
      <div id="securityQuestion">
        <div class="label" id="seq-ques">Question will come here</div>
        <br><input id="input-seq-question" placeholder="Secret Key"/>
      </div>
    </div>
    <br><br>
    <button id="verify"><i class="fab fa-google fa-2x"></i>&nbsp;<span>Verify via Google</span></button>
  </div>
</template>
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
    border: 1px solid #00c8f8;
    height: 20px;
    width: calc( 100% - 40px);
  }
  #verify
  {
    background:transparent;
    padding: 15px;
    border: 1px solid #f8fdff;
    border-radius: 5px;
    width: 210px;
    color: #16b92c;
    display: block;
    margin:auto;
    font-family: 'Aclonica', sans-serif;
    font-size: 15px; 
    cursor: pointer;
    box-shadow: 0px 0px 3px 1px #c1baba;

  }
  

</style>
