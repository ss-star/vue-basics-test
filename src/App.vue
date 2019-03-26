<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <HelloWorld/> -->
    <!-- <Events /> -->
    <Formdata />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Events from './Ement'
import Formdata from './components/form'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Events,
    Formdata
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
