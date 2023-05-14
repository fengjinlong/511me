<template>
  <div class="verifyPage">
    <p class="p">Profile Verification</p>
    <p class="p1">
      Upload a scanned color copy or photo of your identification and get the
      badge!
    </p>
    <el-row class="row1">
      <el-rol class="col1">
        <div class="div">
          <p class="p1">Upload Verification Document Image</p>
          <el-upload
            class="avatar-uploader"
            action="https://660-45f2-925d-ce80ad6c4d15"
            :show-file-list="false"
            :on-success="handleAvatarSuccess"
            :before-upload="beforeAvatarUpload"
          >
            <img v-if="imageUrl" :src="imageUrl" class="avatar-uploader-img" />
            <img
              v-else
              class="avatar-uploader-img"
              src="../../../assets/home/uploadadd1.png"
              alt=""
            />
          </el-upload>
        </div>
        <div class="div">
          <p class="p2">Name</p>
          <el-input v-model="input3" placeholder="" class="input-with">
          </el-input>
        </div>
        <div class="div">
          <p class="p2">ID Number</p>
          <el-input v-model="input3" placeholder="" class="input-with">
          </el-input>
        </div>
        <div class="div">
          <p class="p2"></p>
          <el-button class="btn">SUBMIT</el-button>
        </div>
      </el-rol>
      <el-rol class="col2">
        <div class="line"></div>
        <p class="l1">Accepted Identification</p>
        <p class="l2">
          <img src="../../../assets/home/right-icon.png" alt="" />
          <span>Passport</span>
        </p>
        <p class="l2">
          <img src="../../../assets/home/right-icon.png" alt="" />
          <span>Driver's Licence</span>
        </p>
        <p class="l2">
          <img src="../../../assets/home/right-icon.png" alt="" />
          <span>National ID Card</span>
        </p>
        <p class="l3">
          Acceptable file format: .jpg, .png, .bmp, .gif No PDF or Word
          documents
        </p>
      </el-rol>
    </el-row>
    <p class="bottom">
      <img src="" alt="" />
      <span
        >The information you provide is only used for profile verification and
        is not shared with other members or third parties.</span
      >
    </p>
  </div>
</template>
<script setup>
import { ref } from "vue";

const select = ref("3");
const input = ref("");
const input3 = ref("");
</script>
<style lang="scss" scoped>
.verifyPage {
  padding: 28px 33px;

  .p {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
  }
  .p1 {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #b60038;
    line-height: 26px;
    text-align: center;
    padding: 26px 0;
  }
  .row1 {
    display: flex;
    .col1 {
      .div {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
        .p1 {
          width: 212px;
          height: 52px;
          font-size: 22px;
          font-family: ArialMT;
          color: #000000;
          padding-left: 63px;
          margin-right: 17px;
        }
        .p2 {
          width: 212px;
          height: 26px;
          line-height: 26px;
          font-size: 22px;
          font-family: ArialMT;
          color: #000000;
          padding-left: 63px;
          text-align: right;
          margin-right: 17px;
        }
        .btn {
          width: 260px;
          height: 48px;
          background: #b60038;
          border-radius: 48px;
          font-size: 18px;
          font-family: Arial-BoldMT, Arial;
          color: #ffffff;
          text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }
        .avatar-uploader-img {
          width: 124px;
          height: 124px;
          border-radius: 2px;
        }
      }
      .div.l {
        margin-bottom: 16px;
      }
    }
    .col2 {
      position: relative;
      margin-left: 87px;
      padding-left: 54px;
      .line {
        position: absolute;
        height: 100%;
        background: #eaeaea;
        left: 0;
        top: 58px;
        height: 151px;
        border-left: 1px solid #979797;
      }
      .l1 {
        height: 30px;
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #333333;
        line-height: 30px;
        padding-top: 24px;
        margin-bottom: 15px;
      }
      .l2 {
        display: flex;
        align-items: center;
        // margin-top: 20px;
        img {
          width: 12.5px;
          height: 12.5px;
          margin-right: 6px;
        }
        span {
          height: 29px;
          font-size: 18px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #333333;
          line-height: 28px;
        }
      }
      .l3 {
        width: 207px;
        height: 63px;
        font-size: 15px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #999999;
        line-height: 21px;
        margin-top: 12px;
      }
    }
  }
  .bottom {
    display: flex;
    align-items: center;
    img {
      width: 13.3px;
      height: 12.5px;
      margin-right: 4px;
    }
    span {
      height: 22px;
      font-size: 16px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: #333333;
      line-height: 22px;
    }
  }
}
</style>
<style lang="scss">
.verifyPage {
  .el-input.input-with {
    width: 290px;
    height: 48px;
    background: #ffffff;
    .el-input__wrapper {
      border-radius: 4px;
    }
  }
}
</style>
