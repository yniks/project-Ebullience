<template>
    <div id="LIST-MAIN-CONTAINER">
            <div id="LIST-CONTENT-HOLDER" class="MACRO surface_0">
                <div :active="current==index" tabindex="1" class="LIST-ITEM surface_2 interactive" v-for="(item,index) in data" :key="index"  @focus="current=index">
                    <span :class="'LIST-ICON '" ><img :src="item.icon" v-if="'icon' in item"  /></span>
                    <span class="LIST-TITLE" v-if="!collapsed">{{item.title}}</span>
                </div>
            </div>
    </div>
</template>
<style lang="less" scoped>
[active]
{
    background: black !important;
}
#LIST-MAIN-CONTAINER
{
    .MACRO
    {
        &#LIST-CONTENT-HOLDER
        {
            width:100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            padding:2px;
            .LIST-ITEM
            {  
                margin:2px;
                display: grid;
                grid-template-rows: 1fr;
                grid-template-columns: auto 1fr;
                grid-gap: 4px;
                justify-content: left;
                align-content: center;
                padding:2px;
                .LIST-ICON
                {
                    max-width: var(--surface-logo-length);
                    max-height: var(--surface-logo-length);
                    background-color: transparent;
                    img
                    {
                        width:100%;
                        height:100%;
                        border-radius: 4px;
                    }
                }
                .LIST-TITLE
                {
                    display: grid;
                    place-content: center;
                }
            }
        }

    }
    
}
</style>

<script>
export default {
    props:{
        collapsed:{
            type:Boolean,
            default:false
        },
        list:Array//array of
                /**
                 * {
                 *      *title:String,
                 *      onclick:Function,
                 *      icon:PNG url,
                 *      
                 * }
                 */
    },
    methods: {
    },
    data:()=>
    {
        return {
                current:2,
                data:[
                {
                        title:"Sports Fest",
                        onclick:function(index)
                        {
                            console.log(this);
                        },
                        icon:'http://192.168.43.249:8082/static/img/pramod.jpg'
                },
                {
                        title:"Technical Fest",
                        onclick:function(index)
                        {
                            console.log(this);
                        },
                        icon:'http://192.168.43.249:8082/static/img/pramod.jpg'
                },
                {},
                {
                        title:"Gallery",
                        onclick:function(index)
                        {
                            console.log(this);
                        },
                        icon:'http://192.168.43.249:8082/static/img/pramod.jpg'
                },
        ]}
    }
}
</script>