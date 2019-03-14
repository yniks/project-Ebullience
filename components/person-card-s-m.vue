<template>
    <div :class="'person-card-cont surface_2 '+viewMode"  :style="'background-image:url('+data.image+')'">
                    <div v-if="viewMode=='small-card'" id="image-dp" :style="'background-image:url('+data.image+')'"></div>
                    <dics-viewer :showIndexes="false" title="name" :data="{name:'Pramod dubey',department:'HINDUVATVA',description:'Mandir waheen banayenge!'}" along='vertical' class='person-desc' />
            </div>
</template> 
<style scoped>
    
    .person-card-cont
    {
        width:100%;
        height: 100%;   

        display: grid;
        justify-content: stretch;
        align-content: end;
    }
    #image-dp
    {
        min-width: var(--surface-logo-length);
        min-height:var(--surface-logo-length);
    }
    #image-dp,.person-card-cont
    {
        background: rgba(0,0,0,0.5);
        background-size:cover;
        background-repeat: no-repeat;
        background-position: center
    }
    .medium-card.person-card-cont
    {
        grid-template-columns: 1fr;
    }
    .small-card.person-card-cont
    {
        grid-template-columns: minmax(var(--surface-logo-length),1fr) 2fr;
        grid-template-rows: auto;
        background-image:none !important;
        align-content: center;
    }

    .person-desc
    {
        height:fit-content;
        width:fit-content;
        overflow-y: scroll;
        color: white;
        filter: drop-shadow(0px 0px 16px black);
    }
    /* .medium-card #img
    {
        background-size: cover;
        height: 350px;
        align-items: end;
    } */
</style>
<script>
import dicsViewer from "./dics-viewer"
export default {
    components:{
        dicsViewer
    },
    props:{
        viewMode:String,//small-card,medium-card,huge-card
        data:Object,
    }
}
</script>
