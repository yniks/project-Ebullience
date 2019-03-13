<template>
    <div :class="'surface_0 root '+$mq">
        <div id="title-box">
            <div id="title-container">
                <div id="title-logo">
                    <img src="../assets/niet_logo.png" alt="" srcset="">
                </div>
                <div id="title-Ebullience">Ebullience</div>
                <div id="title-2k19">2K19</div>
            </div>
        </div>
        <div id="main-view-box">
            <div id="main-view-container">
            <component :is="currentView">
             </component>
        </div>
        </div>
    </div>
</template>
<script>
import enterRoll from "./land-enter-rollnumber"
import ebulButton from "./ebul-button"
export default {
    name:"main-container",
    data:()=>
    {
        return {
            currentView:"enter-roll"
        }
    },
    components:{
        enterRoll,
        ebulButton
    }
}
</script>
<style scoped>
.root.ms, .root.bms
{
    grid-template-columns:1fr;
    grid-template-rows: 1fr 2.5fr;
}
.root
{
    display:grid;
    grid-template-columns:1fr 1fr;
    grid-template-rows: 1fr;
    width:100vw;
    height:90vh;
    background:transparent;
}
#main-view-container
{
    width:375px;
    height: 375px;
}
/* #main-view-holder .surface_1
{
    box-shadow: none;
} */
.ms  #title-Ebullience,.bms #title-Ebullience
{
    font-size: 3em;
}
.ms  #title-2k19,.bms #title-2k19
{
    font-size: 1em;
}
#title-Ebullience
{
    font-size: 5vw;
    justify-self: center;
}
#title-2k19
{
    font-size: 2vw;
    justify-self: end
}
#title-box
{
    display: grid;
    justify-items: center;
    align-items: center; 
}
#title-container
{
    height: min-content;
    width:20em;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: min-content min-content;
}
#title-logo
{
    text-align: center
}
#title-logo img
{
   width:50%;
   height: 100%;
}
#main-view-box
{
    display: grid;
    justify-items: center;
    align-items: center;
}

.ls #title-box
{
    width:50vw
}
</style>