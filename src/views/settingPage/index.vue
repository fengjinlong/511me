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
          <el-tab-pane style="width: 124px" label="Account" name="1"
            ><Account
          /></el-tab-pane>
          <el-tab-pane label="Password" name="2">
            <Password />
          </el-tab-pane>
          <el-tab-pane label="Notifications" name="3"> <Notify /> </el-tab-pane>
          <el-tab-pane label="Feedback" name="4">
            <Feedback />
          </el-tab-pane>
          <el-tab-pane label="Contact" name="5"> <Contact /> </el-tab-pane>
        </el-tabs>
      </div>
    </div>
    <el-footer v-if="false">
      <div class="footer">
        <div class="footer-left">
          <div class="logo"></div>
        </div>
        <div class="footer-right">
          <ul>
            <li>About us</li>
            <li>Terms of use</li>
            <li style="margin-right: 169px">Privacy policy</li>
          </ul>
        </div>
      </div>
    </el-footer>
  </div>
</template>
<script setup>
import { computed, ref } from "vue";
// import { useStore } from "vuex";
import Header from "../Home/Header.vue";
import Account from "./account.vue";
import { Search, ArrowRight, ArrowLeft } from "@element-plus/icons-vue";
import Password from "./password.vue";
import Notify from "./notify.vue";
import Contact from "./contact.vue";
import Feedback from "./feedback.vue";
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
  footer {
    width: 100%;
    height: 118px;
    background: #fc3159;

    .footer {
      margin: 34px auto 0;
      height: 118px;
      .footer-left {
        .logo {
          width: 110px;
          height: 33px;
          background: url(../../assets/index/logo.png) no-repeat;
          background-size: cover;
          margin: 41px 68px;
          float: left;
        }
      }

      .footer-right {
        float: right;
        height: 45px;
        margin: 51px 0;
        font-weight: normal;
        color: #ffffff;
        line-height: 16px;

        font-size: 14px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;

        ul {
          li {
            margin: 0 28px;
            display: inline;
          }
        }
      }
    }
  }
}
</style>
