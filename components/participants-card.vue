<template>
    <div class="participant-card-cont surface_2">
        <div class="card-fields-cont">
            <div class="icon card-item">
                <i class="fas fa-user-tie fa-5x user-icon"></i>
            </div>
            <div class="participant-details card-item">
               <span class="participant-name"> {{participant.name}} </span>
               <br><span>&nbsp;&nbsp;&nbsp; Branch: {{participant.branch}}</span>
               <br><span>&nbsp;&nbsp;&nbsp;Events Participated: {{participant.events}}</span>
            </div>        
        </div>    
    </div>    
</template>
<style scoped>
    .participant-card-cont
    {
        background: white;
        color:black;
        width: 100%;
        padding: 15px;
        box-sizing: border-box;
        margin-top:15px;
    }
    .card-fields-cont
    {
        display: grid;
        grid-template-columns: 0.25fr 0.75fr;
        padding: 15px;
    }
    .card-item
    {
        display: grid;
        align-items: center;
    }
    .card-item span
    {
        align-self: center;
    }
    .participant-name
    {
        font-size:2em;
        text-align: center
    }
    .user-icon
    {
        text-align: center;
    }
</style>
<script>
export default {
    components:{},  
    props:{
        participant:Object,branch:String,events:String
    }
}
</script>
