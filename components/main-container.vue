<template>
    <div :class="'surface_0 MAIN-CONTAINER '+$mq+' '+state.view">
        <div id="TITLE-CONTENT-AREA">
            <div id="TITLE-CONTENT-HOLDER">
                <div id="TITLE-nietlogo"><img src="../assets/niet_logo.png" alt="" srcset=""></div>
                <div id="TITLE-ebullience">Ebullience</div>
                <div id="TITLE-2k19">2K19</div>
            </div>
        </div>
        <div id="MAIN-CONTENT-AREA">
                <div id="MAIN-CONTENT-HOLDER">
                    <component :is="currentView" viewMode="medium-card"></component> 
            </div>
        </div>
        <!-- FIXME: FIND A WAY TO BIND ATTRIBUTE. WHY IS IT NOT WORKING NORMALLY? -->
        <list-viewer class="tabs" v-if="state.view=='mainView'" :data-collapsed="$mq=='bms'?'collapsed':'not-collapsed'" :collapsed="$mq=='bms'"/>
    </div>
</template>
<script>
import enterRoll from "./land-enter-rollnumber"
import ebulButton from "./ebul-button"
import photoCard from './photo-card-s-m'
import ebulCard from "./card-s-m"
import personCard from './person-card-s-m'
import thumbViewer from "./list-containers/thumb-viewer"
import listViewer from "./list-viewer"
export default {
    name:"main-container",
    data:function(){
        return {
            data:{
                    image:'http://192.168.43.249:8082/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            currentView:"thumb-viewer"
        }
    },
    components:{
        enterRoll,
        ebulButton,
        personCard,
        photoCard,
        ebulCard,
        thumbViewer,
        listViewer
    }
}
</script>
<style lang="less" >

</style>

<style scoped lang="less">
/**
    ********LANDING STATE VIEW STYLES*******
*/
.landing
{
    &.ms,&.bms
    {
        &.MAIN-CONTAINER
        {
            grid-template-columns:1fr;
            grid-template-rows: 1fr 2.5fr;
            row-gap:10vh;
            #TITLE-CONTENT-AREA
                {
                    img
                    {
                        /**
                            fix logo size in ls mode
                        */
                        width:7em;
                        height: auto;
                    }
                    #TITLE-CONTENT-HOLDER
                    {
                            #TITLE-ebullience
                            {
                                font-size: 3em;
                            }
                            #TITLE-2k19
                            {
                                font-size: 1em;
                            }
                    }
                }
            #MAIN-CONTENT-AREA
                        {
                            #MAIN-CONTENT-HOLDER
                            {
                                width: 90vw;
                                height:100%;
                            }
                        }
        }  
    }
    &.ls
    {
        &.MAIN-CONTAINER
            {
                
                grid-template-columns:1fr 1fr;
                grid-template-rows: 1fr;

                #MAIN-CONTENT-AREA
                        {
                            #MAIN-CONTENT-HOLDER
                            {
                                max-width: 30em;
                                max-height:30em;
                            }
                        }
                #TITLE-CONTENT-AREA
                {
                    img
                    {
                        /**
                            fix logo size in ls mode
                        */
                        width: 9em;
                        height: auto;
                        opacity: 0.89;
                    }
                    #TITLE-CONTENT-HOLDER
                    {
                        
                            filter:drop-shadow(0px 0px 12px #998);
                            text-shadow:0px 0px 12px #998;
                            transform:translateY(-15vh);
                            #TITLE-ebullience
                            {
                                font-size: 5vw;
                                color:#00a4d3;
                            }
                            #TITLE-2k19
                            {
                                font-size: 1em;
                            }
                    }
                }
                
            }
    }
                
    &.MAIN-CONTAINER
    {
            display:grid;
            width:100vw;
            height:100vh;
            background:transparent;
        
            #MAIN-CONTENT-AREA
            {
                display: grid;
                justify-items: center;
                align-items: center;
                #MAIN-CONTENT-HOLDER
                {
                    width: 100%;
                    height:100%;
                }
            }
            #TITLE-CONTENT-AREA
            {
                    display: grid;
                    justify-items: center;
                    align-items: center; 
                
                    #TITLE-CONTENT-HOLDER
                    {
                        height: fit-content;
                        width: fit-content;
                        display: grid;
                        grid-template-columns: 1fr;
                        grid-template-rows: min-content min-content min-content;
                        #TITLE-nietlogo
                        {
                            display: grid;
                            place-content:center;
                        }
                        #TITLE-ebullience
                        {
                            justify-self: center; 
                            color:#36fbf3;   
                        }
                        #TITLE-2k19
                        {
                            font-size: 1em;
                            justify-self: end;
                            color:#46ec8d
                        }
                    }
            }
    }
}
.mainView
{
    
    .tabs
    {
        position: fixed;
        left: 7.4vw;
        width: 15vw;
        top: 39vh;
        &[data-collapsed=collapsed]
        {
            left:-10px;
            top: 45vh;
            width: fit-content;
        }
        &[data-collapsed=not-collapsed]
        {
            min-width:fit-content;
        }
    }
    &.ms,&.bms
    {
        &.MAIN-CONTAINER
        {
            grid-template-columns:1fr;
            grid-template-rows: 1fr 2.5fr;
            row-gap:10vh;
            #TITLE-CONTENT-AREA
                {
                    img
                    {
                        /**
                            fix logo size in ls mode
                        */
                        width:7em;
                        height: auto;
                    }
                    #TITLE-CONTENT-HOLDER
                    {
                            #TITLE-ebullience
                            {
                                font-size: 3em;
                            }
                            #TITLE-2k19
                            {
                                font-size: 1em;
                            }
                    }
                }
            #MAIN-CONTENT-AREA
                        {
                            #MAIN-CONTENT-HOLDER
                            {
                                width: 90vw;
                                height:100%;
                            }
                        }
        }  
    }
    &.ls
    {
        &.MAIN-CONTAINER
            {
                
                grid-template-columns:20vw 1fr;
                grid-template-rows: 1fr;
                #MAIN-CONTENT-AREA
                        {
                            #MAIN-CONTENT-HOLDER
                            {
                                max-width: 90vw;
                                max-height:90vh;
                            }
                        }
                #TITLE-CONTENT-AREA
                {
                    align-content:start;
                    img
                    {
                        /**
                            fix logo size in ls mode
                        */
                        width: 9em;
                        height: auto;
                        opacity: 0.89;
                    }
                    #TITLE-CONTENT-HOLDER
                    {
                            zoom:0.7;
                            filter:drop-shadow(0px 0px 12px #998);
                            text-shadow:0px 0px 12px #998;
                            transform:translateY(7vh);
                            #TITLE-ebullience
                            {
                                font-size: 5vw;
                                color:#00a4d3;
                            }
                            #TITLE-2k19
                            {
                                font-size: 1em;
                            }
                    }
                }
                
            }
    }
                
    &.MAIN-CONTAINER
    {
            display:grid;
            width:100vw;
            height:100vh;
            background:transparent;
        
            #MAIN-CONTENT-AREA
            {
                display: grid;
                justify-items: center;
                align-items: center;
                #MAIN-CONTENT-HOLDER
                {
                    width: 100%;
                    height:100%;
                }
            }
            #TITLE-CONTENT-AREA
            {
                    display: grid;
                    justify-items: center;
                    align-items: center; 
                
                    #TITLE-CONTENT-HOLDER
                    {
                        height: fit-content;
                        width: fit-content;
                        display: grid;
                        grid-template-columns: 1fr;
                        grid-template-rows: min-content min-content min-content;
                        #TITLE-nietlogo
                        {
                            display: grid;
                            place-content:center;
                        }
                        #TITLE-ebullience
                        {
                            justify-self: center; 
                            color:#36fbf3;   
                        }
                        #TITLE-2k19
                        {
                            font-size: 1em;
                            justify-self: end;
                            color:#46ec8d
                        }
                    }
            }
    }
}
        /**
        VERTICAL VIEW
    */

    /**
        HORIZONTAL VIEW
    */
        
            
        
            
            
                
                            
            
</style>