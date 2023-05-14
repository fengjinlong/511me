<template>
  <div class="feedback">
    <el-row class="row">
      <el-rol class="rol1" :span="24">
        <p class="up">Type</p>
        <el-select placeholder="Select" class="feesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <p class="p1">Please fill in your suggestion:</p>
    <el-row class="row">
      <el-rol class="rol1 area" :span="24">
        <el-input
          class="input"
          v-model="input"
          type="textarea"
          placeholder="Please input password"
      /></el-rol>
    </el-row>
    <el-row class="row">
      <el-rol class="rol1" :span="24">
        <p class="up">Upload photos:</p>
        <el-upload
          class="avatar-uploader"
          action="https://run.mocky.io/v3/9d059bf9-4660-45f2-925d-ce80ad6c4d15"
          :show-file-list="false"
          :on-success="handleAvatarSuccess"
          :before-upload="beforeAvatarUpload"
        >
          <img v-if="imageUrl" :src="imageUrl" class="avatar" />
          <img
            v-else
            class="avatar-uploader-icon"
            src="../../assets/home/uploadadd.png"
            alt=""
          />
        </el-upload>
      </el-rol>
    </el-row>
  </div>
</template>
<script setup>
import { ref } from "vue";
import { Plus } from "@element-plus/icons-vue";
const input = ref("");
</script>
<style lang="scss" scoped>
.feedback {
  width: 100%;
  .p1 {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
    padding-top: 40px;
    padding-left: 40px;
    padding-bottom: 20px;
  }

  .row {
    width: 1080px;
    display: flex;
    padding-left: 40px;
    .rol1 {
      flex: 0 0 380px;
      .input {
        width: 100%;
        height: 48px;
        border-radius: inherit;
      }
      .avatar-uploader .avatar {
        width: 178px;
        height: 178px;
        display: block;
      }
      .up {
        height: 25px;
        font-size: 22px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #000000;
        line-height: 26px;
        padding: 40px 0 20px;
      }
    }
    .rol1.area {
      width: 800px;
      height: 240px;
    }
  }
}
</style>
<style lang="scss">
.feedback {
  .el-textarea.input .el-textarea__inner {
    width: 800px;
    height: 240px;
    border-radius: 4px;
    // border: 1px solid #cccccc;
    .el-input__wrapper {
      border-radius: 3px;
    }
  }

  .el-select.feesle {
    width: 500px;
    height: 54px;
    border-radius: 4px;
    border: 1px solid #cccccc;
    .select-trigger {
      width: 100%;
      height: 100%;
      .el-input.el-input--suffix {
        width: 100%;
        height: 100%;
      }
    }
    .el-input__wrapper {
      border-radius: 0;
    }
  }
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
    width: 178px;
    height: 178px;
    text-align: center;
  }
}
</style>
