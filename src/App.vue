<template>
  <img alt="Vue logo" src="./assets/logo.svg">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <firstForm />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import firstForm from './components/firstForm.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    firstForm
  
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
img{
  padding:10px;
  width: 20%;
  height: 20%;
}
</style>
