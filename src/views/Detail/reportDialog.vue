<template>
  <el-dialog class="dialogrep" v-model="centerDialogVisible" width="380" center>
    <img src="../../assets/home/rep.png" alt="" />
    <p class="p">Report Member</p>
    <p class="p1">
      We take steps to ensure that inappropriate or non-genuine profiles are
      removed promptly, however on occasions some slip past us. Help us
      eliminate those by letting us know if you spot something suspicious.
      Please do not use this form to report members you are not interested.
    </p>
    <div class="sel">
      <el-select
        style="width: 100%; height: 100%"
        v-model="value"
        placeholder="Select"
      >
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
    </div>

    <p class="p2">Comments:</p>
    <div class="area">
      <el-input
        v-model="textarea"
        style="border-radius: inherit"
        placeholder="Please input"
        type="textarea"
      />
    </div>
    <el-button class="dialog-btn" @click="Cancel">Submit</el-button>
    <template #footer>
      <el-button class="dialog-btn" @click="Cancel">Submit</el-button>
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
  {
    value: "Option2",
    label: "Option2",
  },

  {
    value: "Option5",
    label: "Option5",
  },
];
</script>
<style lang="scss" scoped>
.dialogrep {
  // padding: 0 20px 20px;
  ::v-deep .el-dialog__body {
    padding-top: 0;
  }
  img {
    width: 76px;
    height: 73px;
    display: block;
    margin: 0 auto;
  }
  .p {
    padding: 14px 0 16px 0;
    text-align: center;
    height: 17px;
    font-size: 16px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 18px;
  }
  .p1 {
    height: 70px;
    font-size: 12px;
    font-family: ArialMT;
    color: #333333;
    line-height: 15px;
    // height: 48px;
  }
  .sel {
    height: 39px;
    background: #f4f4f4;
    border-radius: none;
    margin-top: 15px;
    ::v-deep .el-input__wrapper {
      height: 39px;
    }
  }

  .p2 {
    height: 17px;
    font-size: 16px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 18px;
    padding: 17px 0 9px 0;
  }
  .area {
    height: 79px;
    background: #f4f4f4;

    // border: 1px solid #eaeaea;
    ::v-deep .el-textarea__inner {
      width: 100%;
      border-radius: inherit;
      height: 79px;
      font-size: 14px;
    }
  }
  .dialog-btn {
    width: 256px;
    height: 41px;
    border-radius: 2px;
    background: #b60038;
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
