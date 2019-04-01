<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <HelloWorld/> -->
    <!-- <Events /> -->
    <!-- <Formdata /> -->
    <!-- <first /> -->
    <!-- <parent /> -->
    <!-- <keep /> -->
     <amin /> 
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Events from './Ement'
import Formdata from './components/form'
import first from './components/first'
import parent from './components/sonparent/one'
import keep from './components/comkeep/keep'
import amin from './components/comkeep/amin/amin'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Events,
    Formdata,
    first,
    parent,
    keep,
    amin
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
