<template>
  <div class="backList">
    <div class="div1" v-if="false">
      <div class="btns">
        <el-button class="btn b1">Cancel</el-button>
        <el-checkbox class="cc" v-model="v" label="Select All" />
        <el-button class="btn b2">Delete</el-button>
      </div>
      <div class="list">
        <BlackItem v-for="ele of arr" :key="ele" :ele="ele" />
      </div>
    </div>
    <div class="none">
      <p class="p1">You haven't blocked anyone yet</p>
      <p class="p2">
        If you have received an offensive message or received a message from
        someone that you do not like you can create a "Block" to stop that
        person from contacting you.
      </p>
      <img class="img" src="" alt="" />
      <el-button class="btn">View Matches Now!</el-button>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import BlackItem from "./blackItem.vue";
const arr = [1, 1, 2, 1, 1];
const v = ref(false);
</script>
<style lang="scss" scoped>
.backList {
  .div1 {
    .btns {
      display: flex;
      justify-content: right;
      .btn {
        width: 93px;
        height: 36px;
        background: #b60038;
        border-radius: 4px;
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #ffffff;
      }
      .btn.b1 {
        margin-right: 213px;
      }
      .btn.b2 {
        margin-left: 57px;
      }
    }
    .list {
      width: 1000px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin: 23px auto 0;
      padding: 0 40px;
    }
  }
  .none {
    .p1 {
      height: 34px;
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #000000;
      line-height: 34px;
      text-align: center;
      padding: 25px 0 20px;
    }
    .p2 {
      width: 918px;
      height: 54px;
      font-size: 24px;
      font-family: ArialMT;
      color: #333333;
      line-height: 28px;
      margin: 0 auto;
      padding-bottom: 30px;
    }
    .img {
      width: 413px;
      margin: 0 auto;
      display: block;
      height: 452px;
    }
    .btn {
      width: 350px;
      height: 48px;
      background: #b60038;
      border-radius: 48px;
      font-size: 18px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #ffffff;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
      display: block;
      margin: 40px auto;
    }
  }
}
</style>
<style lang="scss" scoped>
.backList {
  // upload
  .avatar-uploader .el-upload {
    border-radius: 6px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    transition: var(--el-transition-duration-fast);
  }

  .avatar-uploader .el-upload:hover {
    border-color: var(--el-color-primary);
  }

  .avatar-uploader-icon {
    font-size: 28px;
    color: #8c939d;
    width: 170px;
    height: 170px;
    text-align: center;
  }
}
</style>

<style lang="scss">
.backList {
  .el-checkbox.cc {
    .el-checkbox__inner {
      background-color: transparent;
      border: 1px solid #999;
      width: 22px;
      height: 22px;
    }
    .el-checkbox__input {
      width: 22px;
      height: 22px;
      background: #f4f4f4;
      border-radius: 2px;
    }
  }
  .el-checkbox__inner::after {
    border: 2px solid #b60038;
    box-sizing: content-box;
    content: "";
    border-left: 0;
    border-top: 0;
    height: 12px;
    left: 7px;
    position: absolute;
    top: 2px;
    transform: rotate(45deg) scaleY(0);
    width: 6px;
    transition: transform 0.15s ease-in 0.05s;
    transform-origin: center;
  }
  .el-checkbox.cc .el-checkbox__label {
    color: #999;
    height: 30px;
    font-size: 22px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: #333333;
    line-height: 30px;
  }
}
</style>
