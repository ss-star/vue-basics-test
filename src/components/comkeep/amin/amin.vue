<template>
    <div>
        <button v-on:click="Showhide">过渡</button>
        <transition name="fade">
            <p  v-if="show">隐藏</p>
        </transition>
        <transition name="fade2">
            <p v-if="show">移动</p>
        </transition>
        <button @click="showanimation">动画</button>
        <transition name="dong">
            <p  v-if="showaction">嘿嘿</p>
        </transition>
        <button @click="showlibs">动画库</button>
        <!-- //动画会导致回流和重绘，因此动画运动中会出现滚动条，使用定位或浮动可以清除滚动条 -->
         <transition name="hua" class="hua" enter-active-class="animated flipInX" leave-active-class="animated flipOutX">
            <p  v-if="libs">嘿嘿</p>
        </transition>
    </div>
</template>
<script>
export default {
    name:"small1",
    data(){
        return{
           show : true,
           showaction: true,
           libs:true
        }
    },
    methods:{
        Showhide(){
            this.show = !this.show
        },
        showanimation(){
            this.showaction = !this.showaction
        },
        showlibs(){
            this.libs = !this.libs
        }

    }
}
</script>
<style>
/* 动画进入从0~1 */
.fade-enter, .fade-leave-to{
    opacity: 0;
}
 .fade-enter-to, .fade-leave{
    opacity: 1;
} 
.fade-enter-active, .fade-leave-active {
 transition: opacity 1s;
}
.fade2-enter, .fade2-leave-to{
    transform: translate(100px,0)
}
 .fade2-enter-to, .fade2-leave{
    transform: translate(0px,0)
} 
.fade2-enter-active, .fade2-leave-active {
 transition: all 1s;
}

.dong-enter-active{
    animation: bounce-in 1s;
}
 .dong-leave-active{
     animation: bounce-in 1s ease reverse;
 }

@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
p{
    font-size: 40px;
}
</style>

