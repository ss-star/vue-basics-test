<template>
    <div>
        <input v-model="msg">
        <p>{{msg}}</p>
    <div :class="{active:isActive}">你好我好大家好</div> 
   <button v-on:click="formbutton">样式切换</button> 
   <div v-bind:class="[{abc:isActive},'info-'+id]"></div>
   <div class="efg"></div>
   <p :class="{active:index%2 == 0}" v-for="(name,index) in names">{{name}}</p>
    </div>
     
</template>
<script>
export default {
    name:"Formdata",
    data(){
        return {
            msg: "heelo",
            isActive: true,
            id:10,
            names:["lili","xiaoming","huahua","哈哈"]
        }
    },
    // watch:{
    //     msg:function(data){
    //         console.log(data)
    //     }
    
    // },
    methods:{
        formbutton:function(){
            // let isActive = !this.isActive,
             this.isActive = !this.isActive
        }
    }
}
</script>
<style>
 .active{
    color: royalblue;
    font-size: 20px;
}
.abc{
    height: 100px;
    margin-bottom: 80px;
    border: 1px red solid;
}
.efg{
    height: 100px;
    margin-top: 30px;
    border: 2px royalblue solid;
}
</style>
