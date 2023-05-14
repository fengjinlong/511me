<template>
  <div class="passwordset">
    <p class="p1">Reset your password</p>
    <p class="p2">
      To help keep your account secure we recommend that you routinely change
      your password.
    </p>
    <p class="p3">Enter your current password</p>
    <p class="p4">Current Password:</p>
    <el-row class="row">
      <el-rol class="rol1">
        <el-input
          class="input"
          v-model="input"
          type="password"
          placeholder="Please input password"
          show-password
      /></el-rol>
      <el-rol class="rol2">Forgot Password</el-rol>
    </el-row>
    <el-row class="row">
      <el-rol class="rol1">
        <p class="p5">Enter your new password</p>
        <p class="p6">New Password:</p>
        <el-input class="input" v-model="input" type="password" show-password />
        <p class="p6">Confirm New Password:</p>
        <el-input class="input" v-model="input" type="password" show-password />
        <el-button class="btn">SAVE</el-button>
      </el-rol>
      <el-rol class="rol2">
        <div class="tic">
          <p class="p7">Password Guidelines</p>
          <p class="p8">Your password must meet the following criteria:</p>
          <p class="p9">
            <span class="dot"></span>
            <span class="text"
              >Must be greater than 6 characters in length.</span
            >
          </p>
          <p class="p9">
            <span class="dot"></span>
            <span class="text">Must contain at least 1 number.</span>
          </p>
          <p class="p9">
            <span class="dot"></span>
            <span class="text">
              Must not be the same as previous passwords</span
            >
          </p>
        </div>
      </el-rol>
    </el-row>
  </div>
</template>
<script setup>
import { ref } from "vue";
const input = ref("");
</script>
<style lang="scss" scoped>
.passwordset {
  width: 100%;
  .p1 {
    width: 223px;
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
    padding-top: 25px;
    padding-left: 40px;
  }
  .p2 {
    width: 893px;
    height: 22px;
    font-size: 22px;
    font-family: ArialMT;
    color: #666666;
    line-height: 22px;
    padding: 20px 0 40px 40px;
  }
  .p3 {
    width: 301px;
    height: 25px;
    padding-left: 40px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #b60038;
    line-height: 26px;
  }
  .p4 {
    width: 183px;
    height: 25px;
    font-size: 22px;
    font-family: ArialMT;
    color: #000000;
    line-height: 26px;
    padding: 30px 0 24px 40px;
  }

  .row {
    width: 1080px;
    display: flex;
    padding-bottom: 30px;
    padding-left: 40px;
    .rol1 {
      flex: 0 0 380px;
      .input {
        width: 100%;
        height: 48px;
        border-radius: inherit;
      }
      .p5 {
        height: 25px;
        font-size: 22px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #b60038;
        line-height: 26px;
      }
      .p6 {
        height: 25px;
        font-size: 22px;
        font-family: ArialMT;
        color: #000000;
        line-height: 26px;
        padding: 30px 0 8px 0;
      }
      .btn {
        width: 256px;
        height: 48px;
        background: #b60038;
        border-radius: 5px;
        font-size: 18px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #ffffff;
        line-height: 21px;
        text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.2);
        display: block;
        margin: 30px auto;
      }
    }
    .rol2 {
      flex: 1;
      display: flex;
      align-items: center;
      margin-left: 131px;
      .tic {
        width: 395px;
        height: 169px;
        background: #f4f4f4;
        .p7 {
          width: 395px;
          height: 40px;
          line-height: 40px;
          background: #b60038;
          font-size: 18px;
          font-family: ArialMT;
          color: #ffffff;
          text-align: center;
        }
        .p8 {
          font-size: 15px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #333333;
          line-height: 17px;
          text-align: center;
          padding: 14px 0 12px 0;
        }
        .p9 {
          display: flex;
          align-items: center;
          padding-left: 16px;
          .dot {
            flex: 0 0 9px;
            height: 9px;
            border-radius: 9px;
            background: #999999;
            background: url("../../assets/home/iconp.png") no-repeat;
            background-size: cover;
          }
          .text {
            font-size: 15px;
            font-family: ArialMT;
            color: #999999;
            line-height: 24px;
            padding-left: 6px;
          }
        }
      }
    }
  }
}
</style>
<style lang="scss">
.passwordset {
  .el-input.input {
    .el-input__wrapper {
      border-radius: 3px;
    }
  }
}
</style>
