<template>
  <div id="app">
    <headBar/>
    <diaLog ref='diaLog'/>
    <carousel/>
  </div>
</template>

<script>
import HeadBar from './components/HeadBar.vue'
import DiaLog from './components/DiaLog.vue'
import Carousel from './components/Carousel.vue'
export default {
  name: 'app',
  components: {
    headBar:HeadBar,
    diaLog:DiaLog,
    carousel:Carousel
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
