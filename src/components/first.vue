// 父组件向子组件传递数据props,slot(插槽)
<template>
    <div>
        <div class="props">
            <h1>父级(props方式)</h1>
            <input type="text" v-model="ifname">
            <son :title="msg" :ifname="ifname"  :num="num"/>
        </div>
        <div class="slot" >
            <h1>父级(slot方式)</h1>
            <son>
                <div slot="s1">
                    <p>我是插槽内容1</p>
                    <p>多条数据时将slot标签插入div中</p>
                </div>
                
                <p>哈哈哈此时数据不会被显示</p>
                <!-- <p slot="s2">我是插槽2</p> -->
                <p slot-scope="key" slot="s2" class="ptest">{{key.text}}</p>
            </son>
            
        </div>
    </div>
    
</template>
<script>
import son from './son'

export default{
    name:'first',
    data(){
    return{
        msg:'我是父级传递的活数据',
        ifname:'我是初始化',
        num:10,
    }
    },
   
    components:{
        son,
    }
}

</script>
<style>
h1{
    color:red
}
</style>