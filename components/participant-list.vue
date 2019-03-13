<template>
    <div id="participant-list-cont" class="surface_2">
        <div class="header">Participants</div>
        <div class="participant-list">
            <participantsCard :participant="person"/>
            <participantsCard :participant="person"/>
            <participantsCard :participant="person"/>
            <participantsCard :participant="person"/>
            <participantsCard :participant="person"/>
            <participantsCard :participant="person"/>
        </div>     
    </div>   
</template>
<script>
import participantsCard from './participants-card'
export default {
     data:()=>{
    return {
      person:{
        name:"Swapnil Tiwari",
        branch:"CSE",
        events:5
      }
    }
  },
    components:{
        participantsCard
    }
    
}
</script>
<style scoped>
  .header
  {
    text-align: center;
    font-size: 3em;
  }
  #participant-list-cont
  {
    width: 50%;
    display:grid;
    justify-items: center;
    background: white;
    color: black;
  }
  .participant-list
  {
    width: 90%;
    margin-top:10px;
    
  }
</style>


