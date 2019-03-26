<template>
  <div class="hello">
    {{HelloWorld}}
    {{"哈哈哈"}}
    {{0< 10 ? "对的":"错的"}}
    {{"注意：只允许单行语句"}}
    <p v-html="name"></p>
    <p v-text="text"></p>
    <p class="hq">v-bind属性</p>
    <p v-bind:class="hq">v-bind属性</p>
    {{ msg.split('').reverse().join('') }}
    {{mesRs}}                  //计算属性，没有参数不需要带括号
    <div>
      <p v-if="show">if可见</p>
      <p v-else="show">else可见</p>
    </div>
    <div>
      <ul>
        <li v-for="(name,index) in names" v-bind:key="index">{{name}}</li>
      </ul>
      <ul>
        <li v-for="item in user" >
          <span>{{ item.name }}</span>
          </li>
      </ul>
    </div>
    <button v-on:click="num += 1">按钮</button>
    <p>{{num}}</p>
    <button v-on:click="clickbind">按钮事件</button>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  //data中数据的更新会引起视图的更新
  data () {
    
    return {
      num:1,
      HelloWorld:"<p>HelloWorld</p>",
      name:"<p>我是v-html标签</p>",
      text:"<p>我是v-text标签</p>",
      hq:"hq1",
      show:true,
      names:["abc","def","efg"],
      user:[
        {
          id:"0",
          name:"ice",
          age:"20",
        },{
          id:"1",
          name:"ice2",
          age:"21",
        },{
          id:"2",
          name:"ice3",
          age:"22",
        }
      ],
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    clickbind(){
      //this指向当前组件
      //this来索引当前data数据
      this.show = !this.show
    }
  },
  computed:{
    mesRs(){
      return  msg.split('').reverse().join('') 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hq{
  color: red;
}
</style>
