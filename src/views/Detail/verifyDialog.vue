<template>
  <el-dialog
    class="dialogverify"
    v-model="centerDialogVisible"
    width="293"
    center
  >
    <img src="../../assets/home/icon-ver.png" alt="" />
    <p class="p">Verify your number</p>
    <p class="p1">We‘ll send you a confirmation text to verify your number</p>
    <p class="p2 p3">Phone number:</p>
    <div class="sel">
      <el-input
        v-model="input3"
        placeholder="Please input"
        class="input-with-select"
      >
        <template #prepend>
          <el-select class="es" v-model="select" style="border: none">
            <el-option label="+86" value="3" />
          </el-select>
        </template>
        <template #append>
          <el-button class="code">Code</el-button>
        </template>
      </el-input>
    </div>

    <p class="p2">Enter verification code:</p>
    <div class="area">
      <el-input v-model="input" placeholder="Please input" />
    </div>
    <el-button class="dialog-btn" @click="Cancel">Submit</el-button>
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

const select = ref("3");
const input = ref("");
const input3 = ref("");
</script>
<style lang="scss" scoped>
.dialogverify {
  // padding: 0 20px 20px;
  ::v-deep .el-dialog__body {
    padding-top: 0;
  }
  img {
    width: 78px;
    height: 56px;
    display: block;
    margin: 0 auto;
  }
  .p {
    height: 12px;
    font-size: 11px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 13px;
    padding: 11px 0 14px 0;
    text-align: center;
  }
  .p1 {
    // height: 48px;
    font-size: 9px;
    font-family: ArialMT;
    color: #333333;
    line-height: 14px;
    zoom: 0.75;
  }
  .sel {
    height: 30px;
    background: #f4f4f4;
    border-radius: none;
    border: 1px solid #eaeaea;
    // margin-top: 16px;
    ::v-deep .el-input__suffix {
      display: none;
    }
    .es {
      font-size: 10px;
      width: 45px;
      // zoom: 0.8;
    }
    .code {
      width: 70px;
      height: 30px;
      background: #b60038;
      border-radius: 2px;
      font-size: 11px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: #ffffff;
      zoom: 0.8;
    }
  }

  .p2 {
    height: 12px;
    font-size: 11px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 13px;
    padding: 10px 0 7px 0;
  }
  .p2.p3 {
    padding-top: 19px;
  }
  .area {
    background: #f4f4f4;

    border: 1px solid #eaeaea;
    ::v-deep .el-textarea__inner {
      width: 100%;
      border-radius: inherit;
      font-size: 12px;
    }
  }
  .dialog-btn {
    width: 197px;
    height: 25px;
    background: #b60038;
    border-radius: 27px;
    font-size: 9px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #ffffff;
    line-height: 10px;
    display: block;
    text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.2);
    margin: 23px auto 0;
  }
}
</style>
<style lang="scss">
.el-dialog.dialogverify {
  // --el-dialog-padding-primary: -10px;
  .el-dialog__header {
    padding-top: 19px;
  }
  .el-dialog__body {
    padding-top: 0;
    padding-bottom: 25px;
  }
  .el-dialog__footer {
    display: none;
  }
}
</style>
