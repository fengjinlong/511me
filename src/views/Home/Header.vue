dropdownPop
<template>
  <div class="ha">
    <div class="context">
      <div class="logo"></div>
      <ul>
        <li class="item">Online</li>
        <li class="item active">VIP</li>
        <li class="item">Messages</li>

        <el-dropdown popper-class="dropDownStyle">
          <span class="span"> Activity <span class="i">99+</span> </span>
          <template #dropdown>
            <el-dropdown-menu class="dropdownPop">
              <el-dropdown-item>Liked Me<i>2</i></el-dropdown-item>
              <el-dropdown-item>My Likes<i>8</i></el-dropdown-item>
              <el-dropdown-item>Visitors<i>8</i></el-dropdown-item>
              <el-dropdown-item>Block list<i>8</i></el-dropdown-item>
            </el-dropdown-menu>
          </template>
        </el-dropdown>
      </ul>
      <div style="flex-grow: 1" />
      <div class="head"><img src="../../assets/header_bg.jpg" alt="" /></div>
      <el-dropdown class="el-menu-demo">
        <span class="el-dropdown-link"> mumu </span>
        <template #dropdown>
          <el-dropdown-menu class="dropdownPop1">
            <el-dropdown-item>Action 1</el-dropdown-item>
            <el-dropdown-item>Action 2</el-dropdown-item>
            <el-dropdown-item>Action 3</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
      <div class="tick"></div>
      <el-dropdown popper-class="dropDownStyle dropDownStyle2">
        <span class="set"> </span>
        <template #dropdown>
          <el-dropdown-menu class="dropdownPop" slot="dropdown">
            <el-dropdown-item>Account</el-dropdown-item>
            <el-dropdown-item>Password</el-dropdown-item>
            <el-dropdown-item>Notifications</el-dropdown-item>
            <el-dropdown-item>Feedback</el-dropdown-item>
            <el-dropdown-item>Contact Support</el-dropdown-item>
            <el-dropdown-item class="logout">Logout</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>

      <!-- {{ badgeSystem }} -->
    </div>
  </div>
</template>
<script setup>
import { computed } from "vue";
// import { useStore } from "vuex";
// const store = useStore();
// {new: false, cert: false, hot: false}
// const badgeSystem = computed(() => store.state.Badge);
// const badgeSystem = computed(() => store.state.Badge.system);
// console.log(badgeSystem.value);
</script>
<style lang="scss" scoped>
.ha {
  mini-width: 1080px;
  background-color: #b60038;
  .context {
    width: 1080px;
    height: 50px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    .logo {
      width: 119px;
      height: 35px;
      background: url(../../assets/index/logo.png) no-repeat;
      background-size: cover;
      margin-top: -10px;
    }
    ul {
      display: flex;
      // width: 300px;
      // float: left;
      li.item {
        width: 135px;
        height: 50px;
        color: #fff;
        display: flex;
        font-size: 15px;
        justify-content: center;
        align-items: center;
      }
      li.item.active {
        background-color: #ca0b46;
      }
      li.item:hover {
        background-color: #ca0b46;
        cursor: pointer;
        li {
          background-color: #ca0b46;
        }
      }
      // :deep(.el-dropdown.drop):hover {
      //   background-color: #ca0b46;
      //   el-dropdown-menu__item:not(.is-disabled) {
      //     color: red;
      //   }
      // }
    }
    .el-dropdown {
      display: flex;
      align-items: center;
      .span {
        color: #fff;
        width: 135px;
        height: 25px;
        color: #fff;
        display: flex;
        font-size: 15px;
        justify-content: center;
        align-items: center;
        .i {
          position: absolute;
          width: 31px;
          height: 20px;
          border-radius: 10px;
          background: #ffffff;
          color: #ca0b46;
          right: 5px;
          top: 8px;
          font-size: 12px;
          line-height: 20px;
          text-align: center;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
        }
      }
    }
    .dropDownStyle {
      width: 135px;
      height: 50px;
      display: flex;
      font-size: 15px;
      justify-content: center;
      align-items: center;
      .span {
        position: relative;
        i {
          position: absolute;
          width: 20px;
          height: 12px;
          border-radius: 10px;
          background: #ffffff;
          color: #ca0b46;
          right: -9px;
          top: -8px;
          font-size: 12px;
        }
      }
    }
    .head {
      width: 22px;
      height: 22px;
      border-radius: 100%;
      padding: 1px;
      background-color: #fff;
      margin-top: 5px;
      img {
        display: block;
        width: 100%;
        height: 100%;
        border-radius: 100%;
      }
    }
    .el-menu-demo {
      width: 50px;
      height: 33px;
      line-height: 33px;
      border: none;
      color: #fff;
      margin-left: 20px;
      .flex-grow {
        flex-grow: 1;
      }
      :deep .el-sub-menu__title {
        height: 33px;
        background-color: #b60038;
        color: #0e9e86;
      }
      .item {
        height: 33px;
        color: #0b9ba5;
        border: none;
        ::v-deep .el-icon.el-sub-menu__icon-arrow {
          // color: #13b65a;
        }
      }
      .el-menu-item {
        height: 33px;
        color: #fff;
        background-color: #ca0b46;
        position: relative;
        z-index: 9999;
        border: none;
      }
      .el-menu-item.is-active {
        height: 33px;
        background-color: #ca0b46;
      }
      .el-menu-item:hover {
        background-color: #ca0b46;
        height: 33px;
        border: none;
      }
    }
    .tick {
      width: 12px;
      height: 14px;
      background: url(../../assets/home/notice.png) no-repeat;
      background-size: cover;
      margin: 9px;
    }
    .set {
      width: 14px;
      height: 14px;
      margin: 10px;
      background: url(../../assets/home/set.png) no-repeat;
      background-size: cover;
    }
  }
}
</style>

<style lang="scss">
.dropDownStyle {
  background-color: #b60038;
  .dropdownPop {
    background-color: #b60038;
    border-color: red;
  }
  .el-popper__arrow::before {
    content: "";
    display: none;
    background-color: transparent;
  }
  .el-dropdown-menu__item {
    width: 117px;
    height: 31px;
    padding: 0;
    background-color: #b60038;
    padding-left: 18px;
    color: #fff;

    border: none;
    i {
      width: 18px;
      height: 18px;
      border-radius: 100%;
      background: #ffffff;
      color: #ca0b46;
      font-size: 12px;
      margin-left: 4px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: #ca0b46;
      text-align: center;
      font-style: normal;
      line-height: 17px;
    }
  }

  .el-dropdown-menu__item:hover {
    background-color: #ca0b46;
    color: #fff;
    border: none;
  }
}
.dropDownStyle2 {
  .dropdownPop1 {
    background-color: #b60038;
    border-color: red;
  }
  .el-dropdown-menu__item {
    width: 119px;
    height: 31px;
    padding: 0;
    background-color: #b60038;
    padding-left: 11px;
  }
  .el-dropdown-menu__item:last-child {
    height: 45px;
    border-top: 1px solid #ffffff;
  }
}
</style>
