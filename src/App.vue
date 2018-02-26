<template>
  <div id="app">
    <img src="./assets/logo.png">
    <MyComponents/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Events from './components/Event'
import Form from './components/formdata'
import Dd from './components/Dd'
import MyComponents from './components/myComponents'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Events,
    Form,
    Dd,
    MyComponents
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
