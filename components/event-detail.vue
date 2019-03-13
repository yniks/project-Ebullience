<template>
    <div class="event-container surface_2">
        <div class="header">
           <span> Event Name </span>
           <span style="margin-left:70px"> <ebulButton class="event-apply"> Apply </ebulButton> </span>
        </div>
        <hr>
        <div class="details-container">
            <br>
            <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, eligendi vitae assumenda atque quis voluptatum vero architecto corrupti modi dolorum cum amet hic molestias maiores fuga, ratione tempora asperiores delectus ex qui doloribus? Asperiores, doloribus assumenda. Deserunt nemo earum voluptatem voluptatum, aliquam at molestias maiores non eligendi amet unde. Quibusdam repellat quas cum magnam aliquam dolores ut pariatur aliquid illo. Sit quas, blanditiis atque veniam dolorum debitis sint tempore possimus nulla tenetur! Neque ad vitae minima exercitationem eligendi, veniam consequatur ipsum atque deleniti nesciunt cum accusantium nemo praesentium suscipit unde asperiores quo omnis corporis laboriosam doloribus earum, reiciendis eum? Id!</span>
            <br> <br>
            <span> <strong>Time </strong></span>
            <br><br><span> <strong>Venue- NIET </strong></span>
            <br><br><span><strong>Co-ordinators Randi </strong></span>
            <br><br><span><strong>Team Size</strong></span>
        </div>    
        
        
     </div>   
</template>
<script>
import ebulButton from "./button"
export default {
  components:{
    ebulButton
  }
}
</script>
<style scoped>
    @import url('https://use.fontawesome.com/releases/v5.7.2/css/all.css');
    @import url('https://fonts.googleapis.com/css?family=Aclonica');
    @import url('https://fonts.googleapis.com/css?family=Overpass');
    

    .header
    {
        padding:2vw;
        font-size:2em;
        color: #00a4d3;
    }
    .event-container
    {
        padding:20px;
        color:black;
        background:white;
        width: 100%;
    }
    .details-container
    {
         text-align: justify;
    }
    .details-container span
    {
       
        font-family: 'Overpass', sans-serif !important;
    }
    input:focus
    {
        outline-width: 0px;
    }
    button:focus
    {
        outline-width: 0px;
    }
    .event-apply
    {
        background:#10bd10;
        font-size: 20px;
        float:right;
    }


</style>
