<template>
    <div :class="'surface_0 '+along">
        <div class="desc_item" v-for="(item,name) of data" v-bind:key="name">

            <span :id="name+'desc'" class="desc-item-name" v-if="showIndexes">{{name}}</span>
            <span :class="'desc-item '+(title==name?'title':'')">{{item}}</span>

        </div>
    </div>
</template>
<style scoped>
    .desc-item-name
    {
        font-size: 120%;
    }
    .desc-item
    {
         display: grid;
        place-content: stretch;
        width:100%;
        height:100%;
    }
    .title
    {
        font-size: 170%;
        text-transform: capitalize;
    }
    .surface_0
    {
        
        width:100%;
        height:100%;   
    }
    .horizontal 
    {
        place-content: stretch;
        grid-auto-flow: column;;
        grid-auto-rows: auto;
        grid-gap: 1vw;
    }
    .vertical 
    {
        place-content: stretch;
        grid-auto-flow: row;
        grid-auto-columns: auto;
        grid-gap: 0.02em;
    }
</style>

<script>
export default {
    props:{
        title:String,
        along:String,
        showIndexes:Boolean,
        data:Object
    }
}
</script>