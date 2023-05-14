<template>
  <div class="match">
    <p class="up">Edit Match Criteria</p>
    <p class="up1">
      Help us find you the perfect match by telling us what is important to you
      in a partner. Answer the questions below and tell us what you’re looking
      for.
    </p>
    <!-- 1 -->

    <!-- 2 -->
    <el-row class="row">
      <el-rol class="lablem">Country:</el-rol>
      <el-rol class="lablem">State/Province:</el-rol>
    </el-row>
    <!-- 3 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Select" class="matchsle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Select" class="matchsle">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 4 -->
    <el-row class="row row2">
      <el-rol :span="12" class="lablem">Age:</el-rol>
      <el-rol :span="12" class="lablem1">Between Any and Any</el-rol>
    </el-row>
    <!-- 5 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 6 -->
    <el-row class="row row2">
      <el-rol :span="12" class="lablem">Height:</el-rol>
      <el-rol :span="12" class="lablem1">Between Any and Any</el-rol>
    </el-row>
    <!-- 7 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 8 -->
    <el-row class="row row2">
      <el-rol :span="12" class="lablem">Weight:</el-rol>
      <el-rol :span="12" class="lablem1">Between Any and Any</el-rol>
    </el-row>
    <!-- 9 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 10 -->
    <el-row class="row row2">
      <el-rol :span="12" class="lablem">Annual Income:</el-rol>
      <el-rol :span="12" class="lablem1">Between Any and Any</el-rol>
    </el-row>
    <!-- 11 -->
    <el-row class="row">
      <el-rol class="sel">
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
      <el-rol>
        <el-select placeholder="Any" class="matchsle2">
          <el-option label="item.label" value="1" />
        </el-select>
      </el-rol>
    </el-row>
    <!-- 12 -->
    <el-row class="row row2">
      <el-rol :span="12" class="lablem">Education:</el-rol>
    </el-row>
    <!-- 13 -->
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
    <el-button class="btn">SUBMIT</el-button>
  </div>
</template>
<script setup>
import { ref } from "vue";
const input = ref("");
const radio1 = ref("1");
</script>
<style lang="scss" scoped>
.match {
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
    padding: 20px 0 0px;
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
      flex: 0 0 352px;
      padding: 30px 0 20px 0;
    }
    .lablem1 {
      height: 22px;
      font-size: 20px;
      font-family: ArialMT;
      color: #999999;
      line-height: 23px;
      text-align: right;
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
  .row2 {
    width: 632px;
    justify-content: space-between;
  }
}
</style>
<style lang="scss">
.match {
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
    border-radius: 0;
    padding: 28px 29px;
  }

  .el-select.matchsle {
    width: 315px;
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
  .el-select.matchsle2 {
    width: 300px;
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
