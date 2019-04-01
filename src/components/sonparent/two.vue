//子组件向父组件传递数据emit
<template>
    <div>
        子组件
        <button @click="sendson">按钮</button>
    </div>
</template>
<script>
export default {
    name:'child',
    data(){
        return{
            msg:"子组件传递的数据"
        }
    },
    props:{
        num:{
            type:Number,
            default:5
        }
    },
    computed:{
        getnum(){
            return this.num *5
        }
    },
    methods:{
        sendson(event){
            //有两个参数，参数1自定义key，参数2具体数值
            this.$emit("sengmsg",this.getnum)
            //console.log(this.msg)

        }
    }
}
</script>
<style>

</style>


