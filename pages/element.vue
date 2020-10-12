<template>
  <div class="container">
    <el-button @click="dialog">
      ダイアログを開く
    </el-button>
    <el-dialog :visible.sync="visible" title="確認">
      <p>処理されました。</p>
    </el-dialog>
  </div>
</template>

<style lang="css" scoped>
.container {
  text-align: center;
}
</style>

<script>
export default {
  data() {
    return {
      visible: false
    };
  },
  methods: {
    dialog() {
      this.visible = !this.visible;
    }
  }
};
</script>
