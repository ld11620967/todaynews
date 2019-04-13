<template>
  <div>
    <el-input v-model="input" placeholder="请输入用户名" style="margin-bottom: 30px;"></el-input>
    <el-input v-model="input1" placeholder="请输入密码"></el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: ""
    };
  }
};
</script>
