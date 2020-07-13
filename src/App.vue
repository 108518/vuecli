<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">-->
    <HelloWorld msg="欢迎使用 Vue.js App"/>
    <zujian zujianmsg="123456789"/>
    <secondcomponent />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import zujian from './components/zujian.vue'
import secondcomponent from './components/secondcomponent.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    zujian,
    secondcomponent
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
