<template>
  <div class="layout auto-width">
    <div class="left"></div>
    <div id="app">
      <headbar/>
      <dialog1 ref="dialog"/>
      <el-row>
        <el-col :span="18">
            <left/>
        </el-col>
        <el-col :span="6">
          <right/>
        </el-col>
      </el-row>

    </div>
    <div class="right"></div>
  </div>
</template>

<script>
import headbar from "./components/HeadBar.vue";
import dialog1 from "./components/DiaLog.vue";
import left from "./components/Left.vue";
import right from "./components/Right.vue";
export default {
  name: "app",
  components: {
    headbar,
    dialog1,
    left,
    right,
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
