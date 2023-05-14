<template>
  <div class="verif">
    <p class="up">Verify Your Profile And Get The Badge</p>
    <el-row class="row1">
      <el-col class="col1" :span="8">
        <img src="../../../assets/home/1.png" alt="" />
        <span>Get more attention from singles</span>
      </el-col>
      <el-col class="col1" :span="8">
        <img src="../../../assets/home/1.png" alt="" />
        <span>Help improve member safety</span>
      </el-col>
      <el-col class="col1" :span="8">
        <img src="../../../assets/home/1.png" alt="" />
        <span>Become a trusted dater</span>
      </el-col>
    </el-row>
    <!-- 1 -->
    <div v-if="status === 0" class="add">
      <AddModel />
    </div>
    <!-- 2 -->
    <div v-if="status === 2" class="phone">
      <div class="phoneContext">
        <p class="p">Phone number Verification</p>
        <p class="p1">Verify your number and get the badge!</p>
        <p class="t">
          We’ll send you a confirmation text to verify your number
        </p>
        <el-row class="row1">
          <el-rol class="col1">Phone number </el-rol>
          <el-rol class="col2">Please enter the verification code </el-rol>
        </el-row>
        <el-row class="row2">
          <el-rol class="col3">
            <div class="sel">
              <el-input
                v-model="input3"
                placeholder="Please input"
                class="input-p"
              >
                <template #prepend>
                  <el-select class="es" v-model="select" style="border: none">
                    <el-option label="+86" value="1" />
                  </el-select>
                </template>
                <template #append>
                  <el-button class="codea">Code</el-button>
                </template>
              </el-input>
            </div>
          </el-rol>
          <el-rol class="col4">
            <el-input
              v-model="input3"
              placeholder=""
              class="input-code"
            ></el-input>
          </el-rol>
          <el-rol class="col5">
            <el-button class="btn">SUBMIT</el-button>
          </el-rol>
        </el-row>
        <p class="bottom">
          <img src="" alt="" />
          <span
            >The information you provide is only used for profile verification
            and is not shared with other members or third parties.</span
          >
        </p>
      </div>
    </div>
    <!-- 3 -->
    <div v-if="status === 3" class="s1">
      <p class="t1">Profile Verification</p>
      <p class="t2">
        You have 1 document waiting to be verified. We will process this
        document as soon as possible.
      </p>
    </div>
    <!-- 4 -->
    <div v-if="status === 3" class="s1">
      <p class="t1">Phone number Verification</p>
      <p class="t2">
        You have 1 document waiting to be verified. We will process this
        document as soon as possible.
      </p>
    </div>
    <!-- 5 -->
    <div v-if="status === 11" class="s1 s">
      <p class="t1">Phone number Verification</p>
      <p class="t3">Certification completed</p>
    </div>
    <!-- 6 -->
    <div v-if="status === 12" class="s1 s">
      <p class="t1">Phone number Verification</p>
      <p class="t3">Certification completed</p>
    </div>
    <!-- <div v-if="status === 1"></div> -->
    <div v-if="status === 1" class="s1 b">
      <p class="t1">Phone number Verification</p>
      <p class="t3">Certification rejected</p>
      <el-button class="sub">SUBMIT</el-button>
    </div>
    <!-- 6 -->
    <div v-if="status === 1" class="s1 b">
      <p class="t1">Phone number Verification</p>
      <p class="t3">Certification completed</p>
      <el-button class="sub">SUBMIT</el-button>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import AddModel from "./addModel.vue";
const status = ref(1);
const select = ref("1");
const input3 = ref("");
</script>
<style lang="scss" scoped>
.verif {
  width: 1080px;
  padding: 20px 0 0 0;
  .up {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
  }
  .row1 {
    margin-top: 22px;
    display: flex;
    align-items: center;
    margin-bottom: 30px;
    .col1 {
      img {
        width: 15px;
        height: 15px;
        margin-right: 7px;
      }
      span {
        height: 30px;
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #333333;
        line-height: 30px;
      }
    }
  }
  .add {
    width: 1080px;
    // height: 522px;
    background: #f8f8f8;
  }
  .phone {
    width: 1080px;
    // height: 368px;
    background: #f8f8f8;
    margin-top: 24px;
    .phoneContext {
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
        padding: 30px 0 16px 0;
      }
      .t {
        height: 28px;
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: #333333;
        line-height: 28px;
        text-align: center;
      }
      .row1 {
        display: flex;
        align-items: center;
        height: 25px;
        font-size: 22px;
        font-family: ArialMT;
        color: #000000;
        line-height: 26px;
        .col1 {
          flex: 0 0 350px;
          margin-right: 40px;
        }
        .col2 {
          flex: 1;
        }
      }
      .row2 {
        display: flex;
        align-items: center;
        margin-bottom: 35px;
        .col3 {
          flex: 0 0 350px;
          height: 48px;
          background: #ffffff;
          border-radius: 3px;

          .sel {
            height: 48px;

            border: 1px solid #eaeaea;
            .codea {
              width: 70px;
              height: 35px;
              background: #b60038;
              border-radius: 7px;
              font-size: 20px;
              font-family: ArialMT;
              color: #ffffff;
              padding: 0;
            }
          }
        }
        .col4 {
          flex: 0 0 350px;
          height: 48px;
          background: #ffffff;
          border-radius: 3px;
          margin: 0 40px;
        }
        .col5 {
          flex: 1;
          .btn {
            width: 160px;
            height: 48px;
            background: #b60038;
            border-radius: 48px;
            font-size: 18px;
            font-family: Arial-BoldMT, Arial;
            font-weight: normal;
            color: #ffffff;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
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
  }
  .s1 {
    width: 1080px;
    height: 157px;
    background: #f8f8f8;
    margin-bottom: 20px;
    .t1 {
      height: 25px;
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #000000;
      line-height: 26px;
      padding: 28px 0 0 33px;
    }
    .t2 {
      width: 865px;
      height: 50px;
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #666666;
      line-height: 26px;
      margin: 26px 0 0 100px;
    }
    .t3 {
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #b60038;
      line-height: 26px;
      margin: 26px 0 0 100px;
    }
  }
  .s1.s {
    height: 134px;
  }
  .s1.b {
    height: 194px;
    .sub {
      width: 160px;
      height: 48px;
      background: #b60038;
      border-radius: 48px;
      font-size: 18px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #ffffff;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
      margin: 16px 0 0 131px;
    }
  }
}
</style>
<style lang="scss">
.verif {
  .el-input.input-p {
    height: 48px;
    .el-input-group__prepend {
      border-radius: inherit;
      .el-select.es {
        font-size: 20px;
        width: 58px;
        border: none;
        .select-trigger.el-tooltip__trigger.el-tooltip__trigger {
          border: none;
        }
      }
      .el-input__suffix {
        display: none;
      }
      .el-input__wrapper {
        height: 46px;
        border-radius: inherit;
        border: none;
        background-color: #fff;
        box-shadow: 0 0 0 0px;
      }
    }
    .el-input-group__append {
      border-radius: inherit;
      background-color: #fff;
      border: none;
      width: 60px;
    }
    .el-input__wrapper {
      height: 46px px;
      border-radius: inherit;
      font-size: 20px;
      border: none;
      box-shadow: 0 0 0 0px;
    }
    .el-input-group__append {
      box-shadow: 0 0 0 0px;
    }
  }
  .el-input.input-code {
    width: 350px;
    height: 48px;
    background: #ffffff;
    border-radius: 3px;
    // border: 1px solid #eaeaea;
    .el-input__wrapper {
      border-radius: inherit;
      font-size: 20px;
    }
  }
}
// .verif {
//   .el-input.input .el-input__inner {
//     width: 448px;
//     height: 48px;
//     border-radius: 4px;
//     // border: 1px solid #cccccc;
//   }
//   .el-input.input .el-input__wrapper {
//     border-radius: 4px;
//   }
//   .el-textarea.input .el-textarea__inner {
//     width: 998px;
//     height: 189px;
//     background: #f8f8f8;
//     font-size: 22px;
//     font-family: ArialMT;
//     color: #666666;
//     line-height: 26px;
//     border-radius: 0;
//     padding: 28px 29px;
//   }

//   .el-select.matchsle {
//     width: 315px;
//     height: 48px;
//     border-radius: 4px;
//     border-color: #eaeaea;
//     .select-trigger {
//       width: 100%;
//       height: 100%;
//       .el-input.el-input--suffix {
//         width: 100%;
//         height: 100%;
//       }
//     }
//     .el-input__wrapper {
//       border-radius: 0;
//     }
//   }
//   .el-select.matchsle2 {
//     width: 300px;
//     height: 48px;
//     border-radius: 4px;
//     border-color: #eaeaea;
//     .select-trigger {
//       width: 100%;
//       height: 100%;
//       .el-input.el-input--suffix {
//         width: 100%;
//         height: 100%;
//       }
//     }
//     .el-input__wrapper {
//       border-radius: 0;
//     }
//   }
//   .el-radio-group.radi {
//     .el-radio__input .el-radio__inner {
//       width: 20px;
//       height: 20px;
//       background-color: #fff;
//     }
//     .el-radio__input.is-checked .el-radio__inner {
//       width: 20px;
//       height: 20px;
//       border-color: #b60038;
//       background-color: #fff;
//     }
//     .el-radio__inner::after {
//       width: 14px;
//       height: 14px;
//       border-radius: var(--el-radio-input-border-radius);
//       background: #b60038;
//       content: "";
//       position: absolute;
//       left: 50%;
//       top: 50%;
//     }
//     .el-radio__label {
//       color: #999;
//       font-size: 22px;
//       font-family: ArialMT;
//       color: #666666;
//       line-height: 26px;
//     }
//   }
// }
</style>
