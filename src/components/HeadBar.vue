<template>
  <el-row>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em">&nbsp;</div>
    </el-col>
    <el-col :span="8">
      <div style="background:#f9fafc;height:3em">新闻资讯</div>
    </el-col>
    <el-col :span="8">
      
      <div style="background:#f9fafc;height:3em"><i class="el-icon-search"></i>搜索</div>
    </el-col>
    <el-col :span="4">
      <div style="background:#f9fafc;height:3em" @click="showLogin">登录/注册</div>
    </el-col>
    <el-col :span="2">
      <div style="background:#f9fafc;height:3em">&nbsp;</div>
    </el-col>
  </el-row>
</template>

<script>
import Login from './Login'
export default {
  methods:{
    showLogin(){
      this.$parent.$refs.diaLog.showDiaLog(Login);
    }
  }
}
</script>
