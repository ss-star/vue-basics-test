<template>
    <div>
        <input v-model="msg">
        <p>{{msg}}</p>
    
    </div>
</template>
<script>
export default {
    name:"Formdata",
    data(){
        return {
            msg: "heelo"
        }
    },
    watch:{
        msg:function(data){
            console.log(data)
        }
    
    },
    methods:{

    }
}
</script>
<style>

</style>
