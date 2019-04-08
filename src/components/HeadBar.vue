<template>
  <el-row>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">&nbsp;</div>
    </el-col>
    <el-col :span="2">
      <div>
        <img src="https://avatars3.githubusercontent.com/u/15765766?s=460&v=4" height="50px">
        <strong style="padding:10px">逆鳞</strong>
      </div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">首页</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">新闻资讯</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">热门视频</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">搞笑段子</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">图片分享</div>
    </el-col>
    <el-col :span="4">
      <div style="background:#f9fafc;height:3em;line-height:3em">&nbsp;</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">
        <i class="el-icon-search"></i>搜索
      </div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em" @click="showLogin">登录/注册</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em;line-height:3em">&nbsp;</div>
    </el-col>
  </el-row>
</template>

<script>
import Login from "./Login";
export default {
  methods: {
    showLogin() {
      this.$parent.$refs.diaLog.showDiaLog(Login);
    }
  }
};
</script>
