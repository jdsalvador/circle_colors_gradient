<template>
  <P5Circles></P5Circles>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import P5Circles from './components/P5Circles.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld,
    P5Circles
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
</style>
