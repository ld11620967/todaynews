<template>
  <el-dialog title="Nilin的小窝" :visible.sync="dialogVisible" width="400px">
    <component :is="currentView"></component>
    <!-- `checked` 为 true 或 false -->
    <el-checkbox v-model="checked">记住密码</el-checkbox>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <el-button type="text">忘记密码？</el-button>
    </br>
    </br>
    </br>
    <el-button type="primary" round>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      登录
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      </el-button>
    </br>
    <el-button type="text">新用户注册</el-button>
  </el-dialog>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false,
      currentView: null
    }
  },
  methods: {
    showDiaLog(vnode) {
      this.currentView = vnode;
      this.dialogVisible = true;
    }
  }
};
</script>


