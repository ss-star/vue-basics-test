<template>
    <!--在template中只存在一个组件-->
    <div class="event">
        <ul>
            <li v-on:click="getInforname(index,$event)" v-for="(name,index) in rames">{{name}}</li>
        </ul>
    </div>
</template>
<script>
//外部可访问
export default {
    data(){
        return {
            rames:["try","scuure","tyue"],
        }
    },
    methods:{
        //事件中的默认参数是event对象,event是传递的默认参数
        getInforname(data,event){
            console.log(this.rames[data])
            console.log(event)
        }
    }
}
</script>
<style>

</style>
