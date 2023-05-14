<template>
  <el-dialog
    class="dialogrep"
    v-model="centerDialogVisible"
    width="1080"
    center
  >
    <AddModel />
  </el-dialog>
</template>
<script setup>
import { ref } from "vue";
const Props = defineProps({
  centerDialogVisible: Boolean,
});
const centerDialogVisible = ref(Props.centerDialogVisible);
const emit = defineEmits(["update:modelValue"]);
import AddModel from "../edit/verification/addModel.vue";
</script>
<style lang="scss" scoped>
.dialogrep {
  // padding: 0 20px 20px;
}
</style>
<style lang="scss">
.el-dialog.dialogrep {
  // --el-dialog-padding-primary: -10px;
  .el-dialog__header {
    padding-top: 19px;
  }
  .el-dialog__body {
    padding-top: 0;
    padding-bottom: 20px;
  }
  .el-dialog__footer {
    padding-bottom: 20px;
    margin: 0;
    display: none;
  }
}
</style>
