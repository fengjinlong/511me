<template>
  <div class="account">
    <DeleteDialog v-model="dialogVisibleDel" />
    <el-row class="row">
      <el-rol class="rol1">
        <p class="p1">Member ID: 15165619</p>
        <p class="p2">Use this as a reference when you need to contact us.</p>
      </el-rol>
      <el-rol class="rol2">
        <!-- <el-button class="btn">123</el-button> -->
      </el-rol>
    </el-row>
    <el-row class="row">
      <el-rol class="rol1">
        <p class="p1">You’re not a VIP yet!</p>
        <p class="p2">
          Find out all the cool stuff you get when you become VIP. From
          unlimited messaging to more refined searches.
        </p>
      </el-rol>
      <el-rol class="rol2">
        <el-button class="btn">What do I get？</el-button>
      </el-rol>
    </el-row>
    <el-row class="row b">
      <el-rol class="rol1">
        <p class="p1">Delete account</p>
        <p class="p2">
          After permanently deleting your account, all your personal information
          including purchases and messages will be permanently removed and
          unable to be restored. To use okmeete again, you need to re-register,
          re-enter all your information and repurchase VIP.
        </p>
      </el-rol>
      <el-rol class="rol2">
        <el-button class="btn">Delete account</el-button>
      </el-rol>
    </el-row>
  </div>
</template>
<script setup>
import { ref } from "vue";
import DeleteDialog from "./deleteDialog.vue";
const dialogVisibleDel = ref(true);
</script>
<style lang="scss" scoped>
.account {
  width: 100%;

  .row {
    width: 1080px;
    display: flex;
    border-bottom: 1px solid #dfdfdf;
    padding-bottom: 30px;
    padding-left: 40px;
    .rol1 {
      flex: 0 0 634px;
      .p1 {
        font-size: 22px;
        font-weight: 500;
        color: #000000;
        margin-bottom: 17px;
        padding-top: 30px;
      }
      .p2 {
        font-size: 22px;
        // height: 160px;
        font-size: 22px;
        font-family: ArialMT;
        color: #666666;
        line-height: 32px;
      }
    }
    .rol2 {
      flex: 1;
      display: flex;
      align-items: center;
      .btn {
        width: 160px;
        height: 48px;
        background: #b60038;
        border-radius: 3px;
        font-size: 18px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #ffffff;
        margin-left: 193px;
      }
    }
  }
  .row.b {
    border: none;
  }
}
</style>
