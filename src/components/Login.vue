<template>
  <div>
    <el-input v-model="input" placeholder="请输入用户名"></el-input>
    </br>
    </br>
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
