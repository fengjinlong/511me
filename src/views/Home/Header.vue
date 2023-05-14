<template>
  <div class="h">
    <div class="context">
      <div class="logo"></div>
      <ul>
        <li class="item">Online</li>
        <li class="item active">VIP</li>
        <li class="item">Messages</li>
        <el-dropdown class="drop">
          <span class="span"> Activity <i>99</i> </span>
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

      <div class="set"></div>
      <div class="tick"></div>

      <el-dropdown class="el-menu-demo">
        <span class="el-dropdown-link"> mumu </span>
        <template #dropdown>
          <el-dropdown-menu class="dropdownPop">
            <el-dropdown-item>Action 1</el-dropdown-item>
            <el-dropdown-item>Action 2</el-dropdown-item>
            <el-dropdown-item>Action 3</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>

      <div class="head"><img src="../../assets/header_bg.jpg" alt="" /></div>

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
.h {
  mini-width: 1080px;
  background-color: #b60038;
  .context {
    width: 1080px;
    height: 50px;
    margin: 0 auto;
    // display: flex;
    .logo {
      width: 119px;
      height: 35px;
      background: url(../../assets/index/logo.png) no-repeat;
      background-size: cover;
      float: left;
      margin-right: 40px;
    }
    ul {
      display: flex;
      width: 300px;
      float: left;
      li.item {
        width: 76px;
        height: 33px;
        color: #fff;
        display: flex;
        font-size: 11px;
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
      :deep(.el-dropdown.drop):hover {
        background-color: #ca0b46;
        el-dropdown-menu__item:not(.is-disabled) {
          color: red;
        }
      }
    }
    .drop {
      width: 76px;
      height: 33px;
      color: #fff;
      display: flex;
      font-size: 11px;
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
      float: right;
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
      float: right;
      color: #fff;
      margin-left: 20px;
      .flex-grow {
        flex-grow: 1;
      }
      :deep .el-sub-menu__title {
        height: 33px;
        background-color: #b60038;
        color: #fff;
      }
      .item {
        height: 33px;
        color: #fff;
        border: none;
        ::v-deep .el-icon.el-sub-menu__icon-arrow {
          color: #fff;
        }
      }
      .el-menu-item {
        height: 33px;
        color: #fff;
        background-color: #ca0b46;
        position: relative;
        z-index: 9999;
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
      float: right;
      background: url(../../assets/home/notice.png) no-repeat;
      background-size: cover;
      margin: 9px;
    }
    .set {
      width: 14px;
      height: 14px;
      float: right;
      margin: 10px;
      background: url(../../assets/home/set.png) no-repeat;
      background-size: cover;
    }
  }
}
</style>

<style lang="scss">
.dropdownPop {
  background-color: #b60038;

  .el-dropdown-menu__item {
    color: #fff;
    position: relative;
    i {
      position: absolute;
      width: 10px;
      height: 10px;
      border-radius: 100%;
      background: #ffffff;
      color: #ca0b46;
      right: 0;
      top: 0;
      font-size: 12px;
    }
  }
  .el-dropdown-menu__item:hover {
    background-color: #ca0b46;
    color: #fff;
  }
  // .popper__arrow {
  // border: 1px solid #4472cb !important;
  // }
  // .popper__arrow::after {
  //   border-top-color: #46bcff !important;
  //   border-bottom-color: #46bcff !important;
  // }
}
</style>
