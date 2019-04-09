<template>
  <div class="layout auto-width">
    <div class="left"></div>
    <div id="app">
      <headBar/>
      <diaLog ref="diaLog"/>
      <carousel/>
      <list/>
    </div>
    <div class="right"></div>
  </div>
</template>

<script>
import HeadBar from "./components/HeadBar.vue";
import DiaLog from "./components/DiaLog.vue";
import Carousel from "./components/Carousel.vue";
import List from "./components/List.vue";
export default {
  name: "app",
  components: {
    headBar: HeadBar,
    diaLog: DiaLog,
    carousel: Carousel,
    list:List
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 2px;
  width: 1200px;
}
.layout {
  display: flex;
  height: 200px;
  width: 100%;
}
.layout .left {
  flex: 1;
  height: 100%;
}
.layout .right {
  flex: 1;
  height: 100%;
}
</style>
