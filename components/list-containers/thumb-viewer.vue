<template>
    <div :class="'surface_1 thumb-root '+viewMode">
        <div id="list-holder" class="surface_-1">
            <component class="thumb-item" v-for="(item,number) in list" v-bind:key="number" :is="item.type" :data="item" :viewMode="viewMode" ></component>
        </div>
    </div>
</template>
<style lang="less" scoped>
.thumb-root
{
    width: 100%;
    height: 100%;  
     #list-holder
    {
        display: flex;
        width:100%;
        height:100%;
        justify-content: left;
     /**
     TODO:
     */   
        align-content: start;
        flex-flow: row wrap;
        flex-basis: auto;
        overflow: scroll;
        .thumb-item
        {
            margin:6px;
        }
    }
}
.small-card 
{
    .thumb-item
    {
        /**
            fix the dimensions of the card
        */
        width:max-content;
        height:max-content;
    }
}
.medium-card 
{
    .thumb-item
    {
        width:max-content;
        height:370px;
    }
}
</style>
<script>
import eventCardSM from "../event-card-s-m"
import ebulCard from "../card-s-m"
export default {
    props:{
        viewMode:String,//either small-card, medium-card,huge-card
       // list:Array//this array will be distributed to each sub-component, these objects must also include name of subcomponent
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
    },
    data:()=>({
        list:[
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },{
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
            {
                    type:"ebul-card",
                    image:'http://localhost:8081/static/img/pramod.jpg',
                    department:"CSE",
                    desc:'Another photo\'s complete description',
                    fiveWords:'very short descriptioms',
                    uploader:'Some Person',
                    tags:'#pic #picture'
                },
        ]
    }),
    components:{
        eventCardSM,
        ebulCard
    }
}
</script>
