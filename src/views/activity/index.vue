<template>
  <div class="activity">
    <Header />

    <div class="items">
      <div class="tabdiv">
        <div class="point">6</div>
        <el-tabs
          v-model="activeName"
          class="demo-tabs"
          @tab-click="handleClick"
        >
          <el-tab-pane
            style="width: 124px"
            label="Liked Me"
            name="1"
          ></el-tab-pane>
          <el-tab-pane label="My Likes" name="2"></el-tab-pane>
          <el-tab-pane label="Visitors" name="3"></el-tab-pane>
          <el-tab-pane label="Block list" name="4"> </el-tab-pane>
        </el-tabs>
      </div>
      <List v-for="ele of arr" :key="ele" />
      <div class="pagination">
        <el-button
          ><el-icon class="el-icon--left"><ArrowLeft /></el-icon>Prev</el-button
        >
        <el-button>
          Next<el-icon class="el-icon--right"><ArrowRight /></el-icon>
        </el-button>
      </div>
    </div>
    <el-footer>
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
import List from "./list.vue";
import { Search, ArrowRight, ArrowLeft } from "@element-plus/icons-vue";
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
    width: 731px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin: 23px auto 0;
    .tabdiv {
      width: 100%;
      position: relative;
      height: 45px;
      background: #f4f4f4;
      border: 1px solid #dfdfdf;
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
        width: 100%;
        height: 45px;
        background: #f4f4f4;
        :deep(.el-tabs__item) {
          width: 124px;
          height: 45px;
          font-size: 14px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #b60038;
          line-height: 45px;
          text-align: center;
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
          height: 3px;
          background: #b60038;
        }
      }
    }
    .pagination {
      width: 100%;
      display: flex;
      justify-content: space-between;
      .el-button {
        width: 96px;
        height: 30px;
        border-radius: 2px;
        border: 1px solid #b60038;
        font-size: 14px;
        font-family: ArialMT;
        color: #b60038;
      }
      .el-icon--right {
        margin-left: 18px;
      }
      .el-icon--left {
        margin-right: 18px;
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
