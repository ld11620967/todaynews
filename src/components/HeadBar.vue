<template>
  <el-row>
    <el-col :span="3">
      <div>
        <img src="https://avatars3.githubusercontent.com/u/15765766?s=460&v=4" height="50px">
        <strong style="padding:10px">Nilin</strong>
      </div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em">首页</div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em">新闻资讯</div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em">热门视频</div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em">搞笑段子</div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em">图片分享</div>
    </el-col>
    <el-col :span="5">
      <div style="height:3em;line-height:3em">&nbsp;</div>
    </el-col>
    <el-col :span="3">
      <div style="height:3em;line-height:3em">
        <el-input v-model="input" placeholder="请输入内容"></el-input>
      </div>
    </el-col>
    <el-col :span="1">
      <div style="height:3em;line-height:3em">
        <el-button icon="el-icon-search" circle></el-button>
      </div>
    </el-col>
    <el-col :span="2">
      <div style="height:3em;line-height:3em" @click="showLogin">登录/注册</div>
    </el-col>
  </el-row>
</template>

<script>
import Login from "./Login";
export default {
  data() {
    return {
      input: ""
    };
  },
  methods: {
    showLogin() {
      this.$parent.$refs.dialog.showDiaLog(Login);
    }
  }
};
</script>


