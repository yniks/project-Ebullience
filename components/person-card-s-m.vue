<template>
    <div :class="'participant-card-cont surface_2 '+viewMode">
        <div class="card-fields-cont">
            <div class="icon">
                <i class="fas fa-user-tie fa-5x user-icon">X</i>
            </div>
            <div class="participant-details">
               <span class="participant-name participant-detail"> {{data.name}} </span>
               <span class="participant-detail">Department: {{data.department}}</span>
               <span class="participant-detail">Events Participated: {{data.eventsCount}}</span>
            </div>        
        </div>    
    </div>  
</template> 
<style scoped>
.participant-card-cont
{
        min-width: fit-content;
        min-height: fit-content;
        background-color: var(--surface_1_background-color)
}
.card-fields-cont
{
    width:100%;
    height: 100%;;
    display: grid;
    align-items: center;
    justify-items: center;
}
.icon
{
    justify-self: center;
    min-width:50px;
    min-height: 50px;
    display: grid;
    align-content: center;
    justify-content: center;
}
.small-card .card-fields-cont
{
    grid-template-columns:auto auto;
    grid-template-rows:1fr;
}
.medium-card .card-fields-cont
{
      grid-template-columns: auto;
    grid-template-rows: auto auto;
}
.participant-details
{
    filter:drop-shadow(0px 0px 10px var(--surface_2_color));    
    justify-self: center;
    display: grid;
    padding:12px;
    padding:minmax(2px,12px);
    align-content: space-evenly;
    justify-content: spaced-evenly;
}
.participant-name
{
    font-size:2em;
    text-transform: capitalize;
}
</style>
<script>
export default {
    props:{
        viewMode:String,//small-card,medium-card,huge-card
        data:Object,
    }
}
</script>
