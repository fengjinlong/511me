<template>
  <div class="profile">
    <p class="up">Edit Profile</p>
    <p class="up1">
      Answering these profile questions will help other users find you in search
      results and help us to find you more accurate matches. Answer all
      questions below to complete this step.
    </p>
    <!-- 1 -->
    <el-row class="row">
      <el-rol class="lable">First Name:</el-rol>
      <el-rol class="input">
        <el-input
          class="input"
          v-model="input"
          type="text"
          placeholder="Please input"
      /></el-rol>
      <el-rol class="data">Date of Birth:</el-rol>
      <el-rol class="data1">December 23, 1992</el-rol>
    </el-row>
    <!-- 2 -->
    <el-row class="row">
      <el-rol class="lablem">Country:</el-rol>
      <el-rol class="lablem">State/Province:</el-rol>
    </el-row>
    <!-- 3 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Select" class="profilesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Select" class="profilesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 4 -->
    <el-row class="row">
      <el-rol class="lablem">Country:</el-rol>
      <el-rol class="lablem">State/Province:</el-rol>
      <el-rol class="lablem">State/Province:</el-rol>
    </el-row>
    <!-- 5 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Select" class="profilesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol class="sel">
        <el-select placeholder="Select" class="profilesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Select" class="profilesle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 6 -->
    <el-row class="row">
      <el-rol class="lablem">Education:</el-rol>
    </el-row>
    <!-- 7 -->
    <el-row class="row">
      <el-col :span="24">
        <el-radio-group v-model="radio1" class="radi">
          <el-radio label="1">High School </el-radio>
          <el-radio label="2"> Vocational College </el-radio>
          <el-radio label="3">Bachelors Degree </el-radio>
          <el-radio label="4"> Masters Degree </el-radio>
          <el-radio label="5">PhD or Doctorate </el-radio>
        </el-radio-group>
      </el-col>
    </el-row>
    <!-- 8 -->
    <el-row class="row">
      <el-rol class="lablem">Marital Status:</el-rol>
    </el-row>
    <!-- 9 -->
    <el-row class="row">
      <el-col :span="24">
        <el-radio-group v-model="radio1" class="radi">
          <el-radio label="1">Single </el-radio>
          <el-radio label="2"> Divorced </el-radio>
          <el-radio label="3">Widowed </el-radio>
        </el-radio-group>
      </el-col>
    </el-row>
    <!-- 10 -->
    <el-row class="row">
      <el-rol class="lablem">Occupation:</el-rol>
    </el-row>
    <!-- 11 -->
    <el-row class="row">
      <el-col :span="24" class="col11">
        <el-radio-group v-model="radio1" class="radi">
          <el-radio class="radioo" label="1"
            >Administrative / Secretarial / Clerical
          </el-radio>
          <el-radio class="radioo" label="2"> Advertising / Media</el-radio>
          <el-radio class="radioo" label="3"
            >Artistic / Creative / Performance
          </el-radio>
          <el-radio class="radioo" label="4">Construction / Trades </el-radio>
          <el-radio class="radioo" label="5">Education / Academic </el-radio>
          <el-radio class="radioo" label="">Entertainment / Media </el-radio>
          <el-radio class="radioo" label=""
            >Executive / Management / HR
          </el-radio>
          <el-radio class="radioo" label="">IT / Communications </el-radio>
          <el-radio class="radioo" label=""
            >Finance / Banking / Real Estate
          </el-radio>
          <el-radio class="radioo" label=""
            >Fire / law enforcement / security
          </el-radio>
          <el-radio class="radioo" label=""
            >Hair Dresser / Personal Grooming
          </el-radio>
          <el-radio class="radioo" label="">Farming / Agriculture </el-radio>
          <el-radio class="radioo" label=""> Legal</el-radio>
          <el-radio class="radioo" label=""
            >Medical / Dental / Veterinary
          </el-radio>
          <el-radio class="radioo" label="">Military </el-radio>
          <el-radio class="radioo" label=""> Nanny / Child care</el-radio>
          <el-radio class="radioo" label=""
            >No occupation / Stay at home
          </el-radio>
          <el-radio class="radioo" label=""
            >Non-profit / clergy / social services
          </el-radio>
          <el-radio class="radioo" label=""
            >Political / Govt / Civil Service
          </el-radio>
          <el-radio class="radioo" label="">Retail / Food services </el-radio>
          <el-radio class="radioo" label=""> Retired</el-radio>
          <el-radio class="radioo" label="">Sales / Marketing </el-radio>
          <el-radio class="radioo" label=""> Self Employed</el-radio>
          <el-radio class="radioo" label="">Sports / recreation </el-radio>
          <el-radio class="radioo" label="">Student </el-radio>
          <el-radio class="radioo" label=""
            >Technical / Science / Engineering
          </el-radio>
          <el-radio class="radioo" label="">Transportation </el-radio>
          <el-radio class="radioo" label="">Travel / Hospitality </el-radio>
          <el-radio class="radioo" label=""> Unemployed</el-radio>
          <el-radio class="radioo" label="">Other </el-radio>
          <el-radio class="radioo" label="">Domestic Helper </el-radio>
          <el-radio class="radioo" label="">Laborer / Manufacturing </el-radio>
        </el-radio-group>
      </el-col>
    </el-row>

    <!-- 12 -->
    <el-row class="row">
      <el-rol class="lablem">In your own words:</el-rol>
    </el-row>
    <!-- 13 -->
    <el-row class="row">
      <el-rol class="rol1 area" :span="24">
        <el-input
          class="input"
          v-model="input"
          type="textarea"
          placeholder="A little about yourself:"
      /></el-rol>
    </el-row>
    <!-- 1111 -->
    <el-button class="btn">SUBMIT</el-button>
  </div>
</template>
<script setup>
import { ref } from "vue";
const input = ref("");
const radio1 = ref("1");
</script>
<style lang="scss" scoped>
.profile {
  width: 1040px;
  padding: 25px 0 40px 40px;
  .up {
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
  }
  .up1 {
    height: 50px;
    font-size: 22px;
    font-family: ArialMT;
    color: #666666;
    line-height: 26px;
    padding: 20px 0 30px;
  }
  .btn {
    width: 350px;
    height: 48px;
    background: #b60038;
    border-radius: 48px;
    font-size: 18px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #ffffff;
    line-height: 21px;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
    margin: 0 auto;
    display: block;
    margin-top: 50px;
  }

  .row {
    display: flex;
    align-items: center;
    .col11 {
      width: 998px;
      height: 552px;
      padding: 9px 18px;
      background: #f8f8f8;
      .radioo {
        padding: 8px 0;
      }
    }
    .lable {
      flex: 0 0 122px;
      height: 25px;
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #000000;
      line-height: 26px;
      padding-right: 19px;
    }
    .lablem {
      height: 25px;
      font-size: 22px;
      font-family: Arial-BoldMT, Arial;
      font-weight: normal;
      color: #000000;
      line-height: 26px;
      flex: 0 0 328px;
      padding: 30px 0 20px 0;
    }
    .data {
      flex: 0 0 130px;
      height: 25px;
      font-size: 22px;
      font-family: ArialMT;
      color: #000000;
      line-height: 26px;
      margin: 0 19px 0 77px;
    }
    .data1 {
      flex: 1;
      height: 25px;
      font-size: 22px;
      font-family: ArialMT;
      color: #666666;
      line-height: 26px;
    }
    .sel {
      margin-right: 37px;
    }
    // 1111
    .rol1 {
      flex: 0 0 380px;
      .input {
        width: 100%;
        height: 48px;
        border-radius: inherit;
      }
    }
    .rol1.area {
      width: 998px;
      height: 189px;
    }
  }
}
</style>
<style lang="scss">
.profile {
  .el-input.input .el-input__inner {
    width: 448px;
    height: 48px;
    border-radius: 4px;
    // border: 1px solid #cccccc;
  }
  .el-input.input .el-input__wrapper {
    border-radius: 4px;
  }
  .el-textarea.input .el-textarea__inner {
    width: 998px;
    height: 189px;
    background: #f8f8f8;
    font-size: 22px;
    font-family: ArialMT;
    color: #666666;
    line-height: 26px;
    // border: 1px solid #cccccc;
    border-radius: 0;
    padding: 28px 29px;
  }

  .el-select.profilesle {
    width: 290px;
    height: 48px;
    border-radius: 4px;
    border-color: #eaeaea;
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
  .el-radio-group.radi {
    .el-radio__input .el-radio__inner {
      width: 20px;
      height: 20px;
      background-color: #fff;
    }
    .el-radio__input.is-checked .el-radio__inner {
      width: 20px;
      height: 20px;
      border-color: #b60038;
      background-color: #fff;
    }
    .el-radio__inner::after {
      width: 14px;
      height: 14px;
      border-radius: var(--el-radio-input-border-radius);
      background: #b60038;
      content: "";
      position: absolute;
      left: 50%;
      top: 50%;
    }
    .el-radio__label {
      color: #999;
      font-size: 22px;
      font-family: ArialMT;
      color: #666666;
      line-height: 26px;
    }
  }
}
</style>
