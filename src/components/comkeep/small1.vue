<template>
    <div>
{{msg}}
<button @click="changeview">检验缓存</button>
    </div>
</template>
<script>
export default {
    name:"small1",
    data(){
        return{
            msg:"small1"
        }
    },
    methods:{
        changeview(){
            this.msg = "111111"
        }
    }
}
</script>
<style>

</style>

