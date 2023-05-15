<template>
  <div class="home">
    <Header />

    <!-- <ReportDialog v-model="centerDialogVisible" />
    <VipDialog v-model="dialogVisibleVip" />
    <CertifyDialog v-model="dialogVisibleCertify" />
    <VerifyDialog v-model="dialogVisibleVerify" />
    <ProfileDialog v-model="profileDialogVerify" /> -->
    <div class="check">
      <div class="content">
        <div class="image">
          <img class="user" src="../../assets/home/1.png" alt="" />
          <div class="loop">
            <swiper
              :watchSlidesProgress="true"
              :slideToClickedSlide="true"
              :slidesPerView="5"
              @click="slideToClicked"
              class="mySwiper"
            >
              <swiper-slide v-for="(item, index) in 10" :key="index"
                ><img class="s" src="../../assets/home/1.png"
              /></swiper-slide>
            </swiper>
          </div>
        </div>
        <div class="mes">
          <el-row class="row1">
            <el-col class="col1" :span="12">
              <span>Jerry,29</span>
              <img class="vip" src="../../assets/home/vip1.png" alt="" />
              <img class="hot" src="../../assets/home/hot.png" alt="" />
            </el-col>
            <el-col class="col2" :span="12"> </el-col>
          </el-row>
          <el-row class="row2">
            <el-col class="col3" :span="13"
              >ID: 17290635 / Block / Report Member</el-col
            >
            <el-col class="col4" :span="11">
              <div>
                <img src="../../assets/home/like2.png" alt="" />
                <span>Like</span>
              </div>
              <div>
                <img src="../../assets/home/hi.png" alt="" />
                <span>Message</span>
              </div>
            </el-col>
          </el-row>
          <div class="border">
            <el-row class="row3 row4">
              <el-col class="col5" :span="5">Height:</el-col>
              <el-col class="col6" :span="6">170cm</el-col>
              <el-col class="col5" :span="6">Occupation:</el-col>
              <el-col class="col6" :span="7">IT / Communications</el-col>
            </el-row>
            <el-row class="row3">
              <el-col class="col5" :span="5">Weight:</el-col>
              <el-col class="col6" :span="6">80kg</el-col>
              <el-col class="col5" :span="6">Date of Marriage:</el-col>
              <el-col class="col6" :span="7">No Answer</el-col>
            </el-row>
            <el-row class="row3 row4">
              <el-col class="col5" :span="5">Education::</el-col>
              <el-col class="col6" :span="6">Bachelors Degree</el-col>
              <el-col class="col5" :span="6">Have children::</el-col>
              <el-col class="col6" :span="7">No Answer</el-col>
            </el-row>
            <el-row class="row3">
              <el-col class="col5" :span="5">Annual income::</el-col>
              <el-col class="col6" :span="6">$ 30000- $ 45000</el-col>
              <el-col class="col5" :span="6">House:</el-col>
              <el-col class="col6" :span="7">Purchased</el-col>
            </el-row>
            <el-row class="row3 row4">
              <el-col class="col5" :span="5">Star sign:</el-col>
              <el-col class="col6" :span="6">Sagittarius</el-col>
              <el-col class="col5" :span="6">Drink::</el-col>
              <el-col class="col6" :span="7">No Answer</el-col>
            </el-row>
            <el-row class="row3">
              <el-col class="col5" :span="5">Religion:</el-col>
              <el-col class="col6" :span="6">No Answer</el-col>
              <el-col class="col5" :span="6">Car:</el-col>
              <el-col class="col6" :span="7">Purchased</el-col>
            </el-row>
            <el-row class="row3 row4">
              <el-col class="col5" :span="5">Smoke:</el-col>
              <el-col class="col6" :span="6">No Answer</el-col>
              <el-col class="col5" :span="6">Marital Status:</el-col>
              <el-col class="col6" :span="7">No Answer</el-col>
            </el-row>
            <el-row class="row3">
              <el-col class="col5" :span="5">Lives in:</el-col>
              <el-col class="col6" :span="6">China-beijing</el-col>
              <el-col class="col5" :span="6">Nationality:</el-col>
              <el-col class="col6" :span="7">No Answer</el-col>
            </el-row>
          </div>
        </div>
      </div>
      <div class="overview">
        <div class="row">
          <div class="rol1">
            <span>Member Overview</span>
            <img src="../../assets/home/translate.png" alt="" />
          </div>
          <div class="rol2">
            I am a retailer, good memory, very loyal, I like listening to latin
            music, watching television, I love going out for a walk, beach,
            mountain, I love fruits, coffee, desserts, I want to learn another
            language, English, French, Italian, Portuguese, I like to cook, i
            love sunflowers.
          </div>
        </div>
      </div>
      <div class="lookFor">
        <el-row class="row">
          <el-col class="col1" :span="16">She's Looking For</el-col>
          <el-col class="col2" :span="8"
            ><img src="../../assets/home/Verification.png" alt="" />
            Verification</el-col
          >
        </el-row>
        <el-row class="row1">
          <el-col class="col1" :span="6">
            <img src="../../assets/home/Age.png" alt="" />
            <span class="span1">Age：</span>
            <span class="span2">40-45</span>
          </el-col>

          <el-col class="col1 col2" :span="10">
            <img src="../../assets/home/income.png" alt="" />
            <span class="span1">Annual income:</span>
            <span class="span2">$ 30000- $ 45000</span>
          </el-col>

          <el-col class="col1 col2" :span="8">
            <img src="../../assets/home/authentication.png" alt="" />
            <span class="span2 span3">Real name authentication</span>
          </el-col>
        </el-row>
        <!-- 2 -->
        <el-row class="row1">
          <el-col class="col1" :span="6">
            <img src="../../assets/home/Height.png" alt="" />
            <span class="span1">Height:</span>
            <span class="span2">170cm</span>
          </el-col>

          <el-col class="col1 col2" :span="10">
            <img src="../../assets/home/Marital.png" alt="" />
            <span class="span1">Marital Status:</span>
            <span class="span2">No Answer</span>
          </el-col>

          <el-col class="col1 col2" :span="8">
            <img src="../../assets/home/number.png" alt="" />
            <span class="span2 span3">Phone number verified</span>
          </el-col>
        </el-row>
        <!-- 3 -->
        <el-row class="row1">
          <el-col class="col1" :span="6">
            <img src="../../assets/home/Weight.png" alt="" />
            <span class="span1">Weight:</span>
            <span class="span2">80kg</span>
          </el-col>

          <el-col class="col1 col2" :span="18">
            <img src="../../assets/home/Education.png" alt="" />
            <span class="span1">Education:</span>
            <span class="span2">Bachelors Degree</span>
          </el-col>
        </el-row>
        <!-- 4 -->
        <el-row class="row1">
          <el-col class="col1" :span="6">
            <img src="../../assets/home/Lives.png" alt="" />
            <span class="span1 span4">Lives in:</span>
            <span class="span2">China-beijing</span>
          </el-col>

          <el-col class="col1 col2" :span="18">
            <img src="../../assets/home/children.png" alt="" />
            <span class="span1">Have children:</span>
            <span class="span2">No Answer</span>
          </el-col>
        </el-row>

        <el-row class="row2">
          <el-col :span="24">Similar Members </el-col>
        </el-row>
        <el-row>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
        </el-row>
        <el-row>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
        </el-row>
        <el-row>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
        </el-row>
        <el-row>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
          <el-col :span="8"> </el-col>
        </el-row>
      </div>
    </div>
    <div class="items">
      <Item v-for="ele of arr" :key="ele" />
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
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "./swiper.css";
import { computed, ref } from "vue";
// import { useStore } from "vuex";
import Header from "../Home/Header.vue";
import Item from "../Home/Item.vue";
// import ReportDialog from "./reportDialog.vue";
// import VipDialog from "./vipDialog.vue";
// import CertifyDialog from "./certifyDialog.vue";
// import VerifyDialog from "./verifyDialog.vue";
// import ProfileDialog from "./profileDialog.vue";
import { Search, ArrowRight, ArrowLeft } from "@element-plus/icons-vue";
// const store = useStore();
const arr = [1, 1, 1, 1];
const slideToClicked = (e, r) => {
  console.log("e", e.activeIndex);
};

const profileDialogVerify = ref(true);
const centerDialogVisible = ref(false);
const dialogVisibleVip = ref(false);
const dialogVisibleCertify = ref(false);
const dialogVisibleVerify = ref(false);
</script>
<style lang="scss" scoped>
.home {
  min-width: 1080px;

  .check {
    background-color: #fff;
    padding-top: 26px;
  }
  .content {
    width: 718px;
    margin: 0 auto;
    display: flex;
    .image {
      flex: 0 0 238px;
      margin-right: 15px;
      .user {
        width: 238px;
        height: 238px;
      }
      .loop {
        width: 238px;
        height: 40px;
        margin-top: 12px;
      }
    }
    .mes {
      flex: 1;
      .row1 {
        align-items: flex-end;
        .col1 {
          overflow-wrap: break-word;
          color: rgba(0, 0, 0, 1);
          font-family: Arial-BoldMT;
          text-align: left;
          white-space: nowrap;
          display: flex;
          margin-top: 10px;
          span {
            height: 23px;
            font-size: 20px;
            font-family: Arial-BoldMT, Arial;
            font-weight: normal;
            color: #000000;
            line-height: 24px;
          }
          .vip {
            width: 25px;
            height: 12px;
            margin: 6px 0 0 9px;
          }
          .hot {
            width: 11px;
            height: 12px;
            margin: 6px 0 0 7px;
          }
        }
      }
      .row2 {
        margin-bottom: 15px;
        align-items: flex-end;
        .col3 {
          font-size: 14px;
          font-family: ArialMT;
          color: #999999;
        }
        .col4 {
          display: flex;
          justify-content: center;
          margin-top: 5px;
          div {
            width: 93px;
            height: 27px;
            background: #ffffff;
            border-radius: 3px;
            border: 1px solid #b60038;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            margin-left: 16px;
            img {
              width: 17px;
              height: 15px;
              margin-right: 7px;
            }
            span {
              height: 13px;
              font-size: 12px;
              font-family: ArialMT;
              color: #b60038;
              line-height: 14px;
            }
          }
        }
      }
      .border {
        width: 465px;
        height: 209px;
        background: #f4f4f4;
        border-radius: 3px;
        border: 1px solid #d8d8d8;
        .row3 {
          width: 463px;
          height: 26px;
          background: #ffffff;

          .col5 {
            font-size: 11px;
            font-family: PingFangSC-Regular, PingFang SC;
            font-weight: 400;
            color: #999999;
            display: flex;
            align-self: center;
            text-align: right;
            justify-content: right;
          }
          .col6 {
            font-size: 11px;
            font-family: PingFangSC-Regular, PingFang SC;
            font-weight: 400;
            color: #000000;
            display: flex;
            align-self: center;
            padding-left: 9px;
          }
        }
        .row4 {
          background-color: #f4f4f4;
        }
      }
    }
  }
  .overview {
    width: 100%;
    height: 122px;
    background-color: #f4f4f4;
    .row {
      width: 718px;
      margin: 23px auto 0;
      .rol1 {
        display: flex;
        justify-content: space-between;
        padding: 20px 0 11px 0;
        span {
          height: 17px;
          font-size: 16px;
          font-family: Arial-BoldMT, Arial;
          font-weight: normal;
          color: #b60038;
          line-height: 18px;
        }
        img {
          width: 17px;
          height: 17px;
        }
      }
      .rol2 {
        height: 56px;
        font-size: 14px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #666666;
        line-height: 19px;
      }
    }
  }
  .lookFor {
    width: 718px;
    margin: 0px auto;
    .row {
      padding: 23px 0 18px 0;
      .col1 {
        height: 17px;
        font-size: 16px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #b60038;
        line-height: 18px;
      }
      .col2 {
        height: 17px;
        font-size: 16px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #b60038;
        line-height: 18px;
        display: flex;
        img {
          width: 17px;
          height: 17px;
          margin-right: 11px;
        }
      }
    }
    .row1 {
      margin-bottom: 11px;
      .col1 {
        display: flex;
        img {
          flex: 0 0 15px;
          height: 15px;
          margin-right: 11px;
        }
        .span1 {
          flex: 0 0 45px;
          margin-right: 8px;
          height: 16px;
          font-size: 11px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #999999;
          line-height: 16px;
        }
        .span2 {
          flex: 1;
          height: 16px;
          font-size: 11px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #000000;
          line-height: 16px;
        }
        .span3 {
          flex: 1;
        }
        .span4 {
          flex: 0 0 50px;
        }
      }
      .col2 {
        .span1 {
          flex: 0 0 89px;
        }
      }
    }
    .row2 {
      height: 17px;
      font-size: 16px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #b60038;
      line-height: 18px;
      margin: 28px 0 18px 0;
    }
  }
  .items {
    width: 718px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    // margin: 23px auto 0;
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
