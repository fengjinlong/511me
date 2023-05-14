<template>
  <div class="activity">
    <Header />

    <div class="items">
      <p class="s">Settings</p>
      <div class="tabdiv">
        <el-tabs
          v-model="activeName"
          class="demo-tabs"
          @tab-click="handleClick"
        >
          <el-tab-pane style="width: 124px" label="Photos" name="1"
            ><Photos
          /></el-tab-pane>
          <el-tab-pane label="Profile" name="2">
            <Profile />
          </el-tab-pane>
          <el-tab-pane label="Match" name="4">
            <Match />
          </el-tab-pane>
          <el-tab-pane label="Verification" name="5">
            <Verification />
          </el-tab-pane>
        </el-tabs>
      </div>
    </div>
  </div>
</template>
<script setup>
import { computed, ref } from "vue";
// import { useStore } from "vuex";
import Header from "../Home/Header.vue";
import Photos from "./phone.vue";
import Profile from "./profile.vue";
import Verification from "./verification/index.vue";
import Match from "./match.vue";
// const store = useStore();
const arr = [1, 1, 1, 1];
const activeName = ref("1");
const handleClick = (tab, event) => {
  console.log(tab, event);
};
</script>
<style lang="scss" scoped>
.activity {
  min-width: 1080px;

  .items {
    width: 1080px;
    margin: 0 auto;
    margin: 0 auto;
    .s {
      height: 30px;
      font-size: 26px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #000000;
      line-height: 31px;
      padding: 20px 0 19px 0;
    }
    .tabdiv {
      width: 100%;
      width: 1080px;
      position: relative;
      //   height: 59px;
      //   background: #f4f4f4;
      //   border: 1px solid #dfdfdf;
      margin-bottom: 25px;
      .point {
        width: 22px;
        height: 22px;
        background: #b60038;
        border-radius: 50%;
        position: absolute;
        top: -8px;
        left: 86px;
        color: #fff;
        font-size: 12px;
        line-height: 22px;
        text-align: center;
      }
      .demo-tabs {
        width: 1080px;
        :deep(.el-tabs__header.is-top) {
          background-color: #f4f4f4;
        }
        :deep(.el-tabs__item) {
          width: 200px;
          background: #f4f4f4;
          height: 59px;
          font-size: 22px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #333;
          line-height: 59px;
          text-align: center;
          &.is-active {
            color: #b60038;
          }
          // &.is-active::after {
          //   content: "";
          //   border: 11px solid red;
          //   border-radius: 11px;
          //   position: fixed;
          //   z-index: 8888;
          //   top: -4px;
          //   right: 4px;
          // }
        }
        :deep(.el-tabs__active-bar) {
          height: 4px;
          background: #b60038;
        }
      }
    }
  }
}
</style>
