<template>
  <div id="app">
    <headBar/>
    <diaLog ref='diaLog'/>
    <HelloWorld msg="test"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HeadBar from './components/HeadBar.vue'
import DiaLog from './components/DiaLog.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    headBar:HeadBar,
    diaLog:DiaLog
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
  margin-top: 5px;
}
</style>
