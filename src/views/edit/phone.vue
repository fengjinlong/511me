<template>
  <div class="phone">
    <p class="up">Upload photos</p>
    <p class="up1">
      The most effective way to get people to notice you is to add a photo.
    </p>
    <ul class="images">
      <li
        :class="{ image: true, back: ele === 5 ? true : false }"
        v-for="ele of arr"
        :key="ele"
      >
        <img src="../../assets/home/1.png" alt="" />
        <span v-show="ele === 1" class="del"></span>
      </li>
      <el-upload
        class="avatar-uploader"
        action="https://run.mock5d-ce80ad6c4d15"
        :show-file-list="false"
        :on-success="handleAvatarSuccess"
        :before-upload="beforeAvatarUpload"
      >
        <img
          class="avatar-uploader-icon"
          src="../../assets/home/uploadadd.png"
          alt=""
        />
      </el-upload>
    </ul>
    <p class="up">Photo Guidelines</p>
    <p class="up1 u2">How to choose the right primary photo:</p>
    <div class="say">
      <p class="p1">You are smiling :) Photo of just you A recent photo</p>
      <p class="p2">
        Clearly shows your face Good quality and well lit DOES NOT contain
        nudity
      </p>
    </div>
    <img class="example" src="../../assets/home/example.png" alt="" />
  </div>
</template>
<script setup>
import { ref } from "vue";
const arr = ref([1, 1, 1, 5, 1, 1, 1]);
</script>
<style lang="scss" scoped>
.phone {
  width: 1000px;
  padding: 25px 40px 40px;
  .up {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
  }
  .up1 {
    height: 25px;
    font-size: 22px;
    font-family: ArialMT;
    color: #666666;
    line-height: 26px;
    padding: 20px 0 31px 0;
  }
  .up1.u2 {
    padding-bottom: 20px;
  }
  .example {
    width: 400px;
    height: 74.5px;
    margin-top: 30px;
  }
  .say {
    display: flex;
    p {
      height: 96px;
      font-size: 22px;
      font-family: ArialMT;
      color: #666666;
      line-height: 32px;
    }
    .p1 {
      flex: 0 0 181px;
    }
    .p2 {
      flex: 0 0 274px;
      margin-left: 45px;
    }
  }
  .images {
    display: flex;
    flex-wrap: wrap;
    .image {
      width: 170px;
      height: 170px;
      border-radius: 8px;
      border-radius: 6px;
      margin-right: 20px;
      margin-bottom: 20px;
      overflow: hidden;
      position: relative;
      img {
        width: 100%;
        height: 100%;
      }
      span {
        display: block;
        width: 20.8px;
        height: 20.8px;
        background: url("../../assets/home/closeimg.png") no-repeat;
        background-size: 100% 100%;
        position: absolute;
        top: 7px;
        right: 8px;
      }
    }
    .image.back::before {
      content: "";
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      z-index: 8888;
      background: rgba(0, 0, 0, 0.8);
      background: url("../../assets/home/re.png") no-repeat;
      background-size: 100% 100%;
    }
  }
}
</style>
<style lang="scss">
.phone {
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
