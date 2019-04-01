// props子组件接受数据
<template>
<div>
    <div class="son-props">
        <h2>子级组件内容(props方式)</h2>
        子级:{{ title }} -- {{ifname}} --{{num *2}}
    </div>
    <div class="son-slot">
        <h2>子级组件内容(slot方式)</h2>
        <!-- 组件样式可以在父子组建中共同控制 -->
        <slot name="s1"></slot>
        <hr />
        <slot name="s2" text="我是子传父的作用于数据"></slot>        
    </div>
</div>
</template>
<script>
export default {
    name:'son',
    data(){
        return{

        }
    },
    props:{
        title:[String,Number],      //限定父级传递的数据类型，可以设置为多种类型
        ifname:{                        //限定字段是必选项
            type:String,
            required:true,
        },
        num:{
            type:Number,
            default:5,
        }

    }
}
</script>
<style>
h2{
    color: blue
}
</style>


