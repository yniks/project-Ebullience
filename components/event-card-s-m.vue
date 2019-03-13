<template>
    <div :class="'event-card-cont surface_2 '+viewMode">
            <div class="event-details" :style="'background-image:url('+data.image+')'">
               <span class="event-name event-detail"> {{data.name}} </span>
               <span class="event-detail">Department: {{data.department}}</span>
               <span class="event-detail">timing:
                   <span>{{data.timing.from}}</span>
                            to
                    <span>{{data.timing.to}}</span>
               </span>
               <span class="event-detail" id="5-words">{{data.fiveWords}}</span>
            </div>
        </div>  
</template> 
<style scoped>
.event-card-cont
{
        min-width: fit-content;
        min-height: fit-content;
        background-color: var(--surface_1_background-color);
        display: grid;
        place-content: center; 
}
.event-details
{
    width: fit-content;
    height: fit-content;
    filter:drop-shadow(0px 0px 10px var(--surface_2_color));

    display: grid;
    padding:12px;
    padding:minmax(2px,12px);
    align-items: center;
    align-content: space-evenly;
    justify-content: space-evenly;
}
.small-card .event-details
{
    grid-template-rows: 1fr;
    grid-template-columns: repeat(4,1fr);
}
.medium-card .event-details
{
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4,1fr);
    justify-content: center;
    align-content: center;
}
 .event-name
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
