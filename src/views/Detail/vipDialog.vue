<template>
  <el-dialog
    class="dialogvip"
    v-model="centerDialogVisible"
    width="686"
    :show-close="false"
    center
  >
    <el-row class="row">
      <el-col class="rol" :span="8">
        <div class="element">
          <p class="p1">Monthly</p>
          <p class="p2">$49.99</p>
          <p class="line"></p>
          <p class="p3">per month</p>
          <p class="p4"></p>
          <p class="p5">one time charge of $49.99</p>
          <el-button class="btn">Select</el-button>
        </div>
      </el-col>
      <el-col class="rol" :span="8">
        <div class="element year active">
          <span>Best value</span>
          <p class="p1">1 Year</p>
          <p class="p2">$12.51</p>
          <p class="line"></p>
          <p class="p3">per month</p>
          <p class="p4">Save 74.99%</p>
          <p class="p5">one time charge of $149.99</p>
          <el-button class="btn">Select</el-button>
        </div>
      </el-col>
      <el-col class="rol" :span="8">
        <div class="element">
          <p class="p1">6 Months</p>
          <p class="p2">$19.99</p>
          <p class="line"></p>
          <p class="p3">per month</p>
          <p class="p4">Save 59.99%</p>
          <p class="p5">one time charge of $119.99</p>
          <el-button class="btn">Select</el-button>
        </div>
      </el-col>
    </el-row>
    <template #footer> </template>
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
.dialogvip {
  .row {
    .rol {
      display: flex;
      align-items: center;
      .element {
        width: 198px;
        height: 285px;
        background: #ffffff;
        border-radius: 4px;
        border: 1px solid transparent;
        p {
          text-align: center;
        }
        .p1 {
          height: 20px;
          font-size: 18px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #b60038;
          line-height: 20px;
          padding-top: 30px;
        }
        .p2 {
          height: 19px;
          font-size: 29px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #000;
          line-height: 19px;
          margin: 17px 0 22px 0;
        }
        .line {
          width: 170px;
          height: 1px;
          background: #e8edfa;
          margin: 0 auto;
        }
        .p3 {
          margin: 12px 0 14px 0;
          height: 16px;
          font-size: 12px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #999990;
          line-height: 16px;
        }
        .p4 {
          margin-bottom: 18px;
          height: 25px;
          font-size: 18px;
          font-family: Arial-BoldItalicMT, Arial;
          font-weight: normal;
          color: #b60038;
          line-height: 20px;
        }
        .p5 {
          margin-bottom: 24px;
          height: 16px;
          font-size: 12px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #999990;
          line-height: 16px;
        }
        .btn {
          display: block;
          margin: 0 auto;
          width: 124px;
          height: 33px;
          background: #b60038;
          border-radius: 2px;

          font-size: 15px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #ffffff;
          text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }
      }
      .element.year {
        position: relative;
        span {
          position: absolute;
          background: #b60038;
          font-size: 10px;
          font-family: Arial-BoldItalicMT, Arial;
          font-weight: normal;
          color: #ffffff;
          line-height: 28px;
          text-align: center;
          top: -14px;
          left: 57px;

          width: 83px;
          height: 29px;
          border-radius: 15px;
        }
      }
      .element.active {
        border: 1px solid #eaeefb;
        box-shadow: 0px 2px 17px 0px rgba(232, 237, 250, 1);
      }
    }
  }
}
</style>

<style lang="scss">
.el-dialog.dialogvip {
  // --el-dialog-padding-primary: -10px;
  .el-dialog__header {
    height: 45px;
    padding: 0;
  }
  .el-dialog__body {
    padding-top: 0;
    padding-bottom: 39px;
  }
  .el-dialog__footer {
    padding-bottom: 0px;
    margin: 0;
    display: none;
  }
}
</style>
