<template>
    <div>
        keep-alive
        <!-- {{currentview}} -->
        <keep-alive>
            <component :is="currentview"></component>
        </keep-alive>
        <button @click="changekeep">作用域切换</button>
        
    </div>
</template>
<script>
import small1 from './small1'
import small2 from './samll2'
export default {
    name:"keep",
    data(){
        return{
            currentview:'small1',
            currentview2:'small2',
            flag:true
        }
    },
    components:{
        small1,
        small2
    },
    methods:{
        changekeep(){
            if(this.flag){
                this.currentview = "small2"
                this.flag = false
            }
            else{
                this.currentview = "small1"
                this.flag = true
            }
            
        }
    }
}
</script>
<style>

</style>

