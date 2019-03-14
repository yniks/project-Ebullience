<template>
    <div :class="'card-cont surface_1 '+viewMode"  :style="'background-image:url('+data.image+')'">
                    <div v-if="viewMode=='small-card'" id="image-dp" :style="'background-image:url('+data.image+')'"></div>
                    <dics-viewer :showIndexes="false" title="name" :data="{name:data.uploader,department:data.department,description:data.fiveWords,tags:data.tags}" along='vertical' class='desc' />
            </div>
</template> 
<style scoped>
    .card-cont
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
    #image-dp,.card-cont
    {
        background: rgba(255,255,255,5);
        background-size:cover;
        background-repeat: no-repeat;
        background-position: center
    }
    .medium-card.card-cont
    {
        grid-template-columns: 1fr;
    }
    .small-card.card-cont
    {
        grid-template-columns: minmax(var(--surface-logo-length),1fr) 2fr;
        grid-template-rows: auto;
        background-image:none !important;
        align-content: center;
    }
    .desc
    {
        height:fit-content;
        width:fit-content;
        overflow-y: scroll;
        color: white;
        filter: drop-shadow(0px 0px 16px black);
    }
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
