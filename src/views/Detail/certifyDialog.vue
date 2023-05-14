<template>
  <el-dialog
    class="dialogcertify"
    v-model="centerDialogVisible"
    width="336"
    :show-close="false"
    center
  >
    <div class="bg">
      <p class="p1">1year</p>
      <p class="p2">$19.99</p>
    </div>

    <div class="element">
      <img src="../../assets/home/ok1.png" alt="" />
      <p class="p1">Increase exposure tenfold</p>
    </div>
    <div class="element">
      <img src="../../assets/home/ok1.png" alt="" />
      <p class="p1">Daily chat with five members of the opposite sex</p>
    </div>
    <div class="element">
      <img src="../../assets/home/ok1.png" alt="" />
      <p class="p1">More people see you</p>
    </div>

    <template #footer>
      <el-button class="btn">Select</el-button>
    </template>
  </el-dialog>
</template>
<script setup>
import { ref } from "vue";
const Props = defineProps({
  centerDialogVisible: Boolean,
});
const centerDialogVisible = ref(Props.centerDialogVisible);
const emit = defineEmits(["update:modelValue"]);

const Cancel = () => {
  emit("update:modelValue", false);
};

const value = ref("");
const textarea = ref("");

const options = [
  {
    value: "Option1",
    label: "Option1",
  },
];
</script>

<style lang="scss" scoped>
.dialogcertify {
  width: 336px;
  height: 387px;
  display: flex;
  align-items: center;
  --el-dialog-padding-primary: -10px;
  .bg {
    width: 336px;
    height: 137px;
    background: #b60038;
    border-radius: 3px 3px 0px 0px;
    .p1 {
      height: 23px;
      font-size: 18px;
      font-family: Helvetica-Bold, Helvetica;
      font-weight: bold;
      color: #ffffff;
      line-height: 23px;
      letter-spacing: 1px;
      padding: 25px 0 18px 0;
      text-align: center;
    }
    .p2 {
      height: 46px;
      font-size: 40px;
      font-family: Roboto-Bold, Roboto;
      font-weight: bold;
      color: #ffffff;
      line-height: 46px;
      letter-spacing: 1px;
      text-align: center;
    }
  }
  .element {
    padding: 23px 47px 0 42px;
    background: #ffffff;
    display: flex;
    align-items: center;
    img {
      flex: 0 0 18px;
      height: 13px;
      margin-right: 19px;
    }

    .p1 {
      font-size: 14px;
      font-family: Helvetica;
      color: #0d253e;
      line-height: 20px;
      flex: 1;
    }
  }
  .btn {
    width: 257px;
    height: 42px;
    background: #b60038;
    border-radius: 3px;
    font-size: 13px;
    font-family: Helvetica;
    color: #ffffff;
    line-height: 16px;
    letter-spacing: 1px;
  }
}
</style>
<style lang="scss">
.el-dialog.dialogcertify {
  --el-dialog-padding-primary: -10px;
  .el-dialog__header {
    display: none;
  }
  .el-dialog__body {
    padding-top: 0;
  }
  .el-dialog__footer {
    padding-bottom: 30px;
  }
}
</style>
