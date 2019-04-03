<template>
  <el-dialog title="提示" :visible.sync="dialogVisible" width="30%">
    <component :is="currentView"></component>
    <span>忘记密码</span>
    <span slot="footer" class="dialog-footer">
      <el-button type="primary" @click="dialogVisible = false">登 录</el-button>
      <el-button @click="dialogVisible = false">注 册</el-button>
    </span>
  </el-dialog>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false,
      currentView: null
    };
  },
  methods: {
    showDiaLog(vnode) {
      this.currentView = vnode;
      this.dialogVisible = true;
    }
  }
};
</script>


