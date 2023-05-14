<template>
  <el-dialog
    class="deleteDialog"
    v-model="centerDialogVisible"
    width="520"
    center
  >
    <img src="../../assets/home/del_i.png" alt="" />
    <p class="p del">Delete account</p>
    <p class="p">We’re sad to see you go</p>
    <p class="p1">Let us know why you want to delete your account</p>
    <div class="choose">
      <div class="line">
        <el-checkbox class="box" v-model="checked1" />
        <p>I found someone</p>
      </div>
      <div class="line">
        <el-checkbox class="box" v-model="checked" />
        <p>Didn't find anyone interesting</p>
      </div>
      <div class="line">
        <el-checkbox class="box" v-model="checked" />
        <p>Too expensive</p>
      </div>
      <div class="line">
        <el-checkbox class="box" v-model="checked" />
        <p>Site is hard to use</p>
      </div>
      <div class="line">
        <el-checkbox class="box" v-model="checked" />
        <p>No one replies</p>
      </div>
      <div class="line">
        <el-checkbox class="box" v-model="checked" />
        <p>Other</p>
      </div>
    </div>

    <el-button class="dialog-btn" @click="Cancel">Next</el-button>
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

const checked1 = ref(true);
const textarea = ref("");
</script>
<style lang="scss" scoped>
.deleteDialog {
  // padding: 0 20px 20px;
  ::v-deep .el-dialog__body {
    padding-top: 0;
  }
  img {
    width: 172px;
    height: 143px;
    display: block;
    margin: 0 auto;
  }
  .p {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
    text-align: center;
  }
  .p.del {
    padding: 16px 0 4px 0;
  }
  .p1 {
    height: 22px;
    font-size: 20px;
    font-family: ArialMT;
    color: #333333;
    line-height: 23px;
    padding: 8px 0 20px 0;
    text-align: center;
  }
  .choose {
    padding-left: 70px;
    .line {
      display: flex;
      align-items: center;
      padding-bottom: 20px;
      .box {
        flex: 0 0 16px;
        height: 16px;
      }
      p {
        flex: 1;
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #666666;
        line-height: 28px;
        padding-left: 26px;
      }
    }
  }

  .p2 {
    height: 12px;
    font-size: 11px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 13px;
    padding: 14px 0 7px 0;
  }

  .dialog-btn {
    width: 350px;
    height: 48px;
    background: #b60038;
    border-radius: 48px;
    display: block;
    margin: 0 auto;

    font-size: 18px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #ffffff;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
  }
}
</style>
<style lang="scss">
.el-dialog.deleteDialog {
  // --el-dialog-padding-primary: -10px;
  .el-dialog__header {
    padding-top: 19px;
  }
  .el-dialog__body {
    padding-top: 0;
    padding-bottom: 30px;
  }
  .el-dialog__footer {
    padding-bottom: 20px;
    margin: 0;
    display: none;
  }
}
.el-checkbox.is-checked.box {
  .el-checkbox__inner {
    background-color: transparent;
    border: 1px solid #999;
  }
}
.el-checkbox__inner::after {
  border: 1px solid #999;
  box-sizing: content-box;
  content: "";
  border-left: 0;
  border-top: 0;
  height: 7px;
  left: 4px;
  position: absolute;
  top: 1px;
  transform: rotate(45deg) scaleY(0);
  width: 3px;
  transition: transform 0.15s ease-in 0.05s;
  transform-origin: center;
}
</style>
