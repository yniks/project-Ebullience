<template>
    <div :class="'photo-card-cont surface_2 '+viewMode" id="img" :style="'background-image:url('+data.src+')'">
                    <div v-if="viewMode=='small-card'" id="image-dp" :style="'background-image:url('+data.src+')'"></div>
                    <dics-viewer :showIndexes="false" :data="{uPloader:'Some One',dec:' ;iuwebh; fispdf o;iwhefiuhwe;ufuwhe; u fw;eu f;wu; efygw;e'}" along='vertical' class='photo-desc' />
            </div>
</template> 
<style scoped>
    
    .photo-card-cont
    {
        width:400px;
        height: 400px;
        display: grid;
        justify-content: stretch;
        align-content: flex-end;
        background: rgba(0,0,0,0.5);
        background-repeat: no-repeat;
        background-position: center
    }
    #image-dp
    {
        min-width: 10em;
        min-height: 10em;
    }
    .medium-card .photo-card-cont
    {
        grid-template-columns: 1fr;
        grid-template-rows: repeat(auto-fit,1fr);
    }
    .small-card .photo-card-cont
    {
        grid-template-columns: auto auto;
        grid-template-rows: auto;
    }

    .photo-desc
    {
        height:fit-content;
        width:fit-content;
        overflow-y: scroll;
        color: floralwhite;
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
