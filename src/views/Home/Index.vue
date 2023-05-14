<template>
  <div class="home">
    <Header />

    <div class="check">
      <div class="content">
        <el-row>
          <el-col :span="12">
            <div class="search">
              <el-input
                v-model="input2"
                placeholder="Please Input"
                :suffix-icon="Search"
              /></div
          ></el-col>
          <el-col :span="12" style="display: flex"
            ><span class="label">Annual Income</span>
            <div class="search search2">
              <div v-if="mask" class="mask">
                <img src="../../assets/home/lock.png" alt="" />
              </div>
              <el-select
                v-else
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
          </el-col>
        </el-row>
        <el-row style="margin: 26px 0">
          <el-col :span="8" style="display: flex">
            <span>Country/Region</span>
            <div class="search search3">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select></div
          ></el-col>
          <el-col :span="8" style="display: flex"
            ><span style="margin-left: 48px">State</span>
            <div class="search3 search">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
          </el-col>
          <el-col :span="8" style="display: flex"
            ><span>Education</span>
            <div class="search4 search">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
          </el-col>
        </el-row>
        <!-- 3 -->
        <el-row>
          <el-col :span="8" style="display: flex">
            <span>Height</span>
            <div class="search search5">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
            <span style="margin: 0 18px; height: 30px; line-height: 30px">
              -
            </span>
            <div class="search5 search">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
          </el-col>
          <el-col :span="8" style="display: flex"
            ><span>Age</span>
            <div class="search5 search">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
            <span style="margin: 0 18px; height: 30px; line-height: 30px">
              -
            </span>
            <div class="search5 search">
              <el-select
                v-model="income"
                filterable
                placeholder="Select"
                style="font-size: 16px"
              >
                <el-option
                  v-for="item in incomes"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value"
                />
              </el-select>
            </div>
          </el-col>
          <el-col :span="8">
            <el-button
              style="
                width: 141px;
                height: 30px;
                background: #b60038;
                border-radius: 2px;
                font-size: 14px;
                font-family: Arial-BoldMT, Arial;
                font-weight: normal;
                color: #ffffff;
                float: right;
              "
              >Show matches</el-button
            ></el-col
          >
        </el-row>
      </div>
    </div>
    <div class="items">
      <Item v-for="ele of arr" :key="ele" />
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
import Header from "./Header.vue";
import Item from "./Item.vue";
import { Search, ArrowRight, ArrowLeft } from "@element-plus/icons-vue";
// const store = useStore();
const incomes = [{ value: "1", label: "全部" }];
const income = "";
const input2 = ref("");
const arr = [1, 1, 1, 1, 1, 1, 1, 1, 1, 1];
const mask = ref(true);
</script>
<style lang="scss" scoped>
.home {
  min-width: 1080px;

  .check {
    background-color: #eee;
    padding-top: 26px;
    .content {
      width: 786px;
      margin: 0 auto;
      padding-bottom: 14px;
      .search {
        width: 347px;
        background: #ffffff;
        border-radius: 2px;
        ::v-deep .el-input--suffix {
          height: 30px;
        }
      }
      .mask {
        width: 236px;
        height: 100%;
        background: #d8d8d8;
        opacity: 0.95;
        display: flex;
        justify-content: center;
        align-items: center;
        img {
          width: 15px;
          height: 17px;
        }
      }
      .search2 {
        width: 236px;
        height: 30px;
        ::v-deep .el-select {
          height: 30px;
        }
      }
      .search3 {
        width: 147px;
        height: 30px;
        ::v-deep .el-select {
          height: 30px;
        }
      }
      .search4 {
        width: 280px;
        height: 30px;
        ::v-deep .el-select {
          height: 30px;
        }
      }
      .search5 {
        width: 76px;
        height: 30px;
        ::v-deep .el-select {
          height: 30px;
        }
      }
      span {
        font-size: 14px;
        font-family: ArialMT;
        color: #000000;
        margin: 8px 10px 7px 0px;
        .l {
          margin-left: 48px;
        }
      }
    }
  }
  .items {
    width: 786px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin: 23px auto 0;
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
