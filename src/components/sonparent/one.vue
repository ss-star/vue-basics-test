//父组件接受子组件传递数据emit
<template>
    <div>
        父组件
        <input type="text" v-model="num">
        <child @sengmsg="getmsg" :num="getnum"/>
        {{msg}}
    </div>
</template>
<script>
import  child from './two'
export default {
    
    name:'parent',
    data(){
        return{
            msg:"初始化",
            num:5
        }
    },
    computed:{
        getnum(){
            return this.num - 0;
        }
    },
    components:{
        child
    },
    methods: {
        getmsg(data){
            this.msg = data 
            //console.log(data)
        }
    },
}
</script>
<style>

</style>


