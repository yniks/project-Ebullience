<template>
    <div :class="'surface_0 root '+viewode">
        <div id="list-holder">
        <div v-for="(number,item) in list" v-bind:key="number"><component :is="item.type" :data="item"></component></div>
        </div>
    </div>
</template>
<style scoped>
.root #list-holder
{
    display: grid;
}
.small-card #list-holder
{
    grid-template-columns: 1fr  ;
    grid-row-gap: auto;
    grid-auto-rows: minmax(50px,1fr);
    grid-auto-columns: minmax(150px,1fr);
    align-content: space-evenly;
    justify-content: space-evenly;
}
.medium-card #list-holder
{
    grid-template-columns: 1fr;
    grid-row-gap: auto;
    grid-auto-rows: minmax(150px,1fr);
    grid-auto-columns: minmax(150px,1fr);
    align-content: space-evenly;
    justify-content: space-evenly;
}
.huge-card #list-holder
{
    grid-template-columns: 1fr;
    grid-row-gap: auto;
    grid-auto-rows: 100%;
    grid-auto-columns: 100%;
    align-content: space-evenly;
    justify-content: space-evenly;
}
</style>
<script>
export default {
    props:{
        viewMode:String,//either small-card, medium-card,huge-card
        list:Array//this array will be distributed to each sub-component, these objects must also include name of subcomponent
                // either [person-card,event-card,photo-card]
                /**
                 * example of list [{
                 *         *type:"person-card",
                 *          name:"",
                 *          branch:"",
                 *          year:""
                 *         ..etc
                 * }]
                 */
    }
}
</script>
