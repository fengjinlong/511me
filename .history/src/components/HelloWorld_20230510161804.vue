<template>
  <div class="con">
    <div v-for="ele of list" :key="ele" class="item">
      <img src="./1.png" alt="" />
      <div class="name">
        <span>Jerry,29</span>
        <img class="vip" src="" alt="" />
        <img class="hot" src="" alt="" />
      </div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </div>
</template>
<script setup>
const list = [1, 2, 3, 4, 5, , 1, 1, 1, 1];
</script>
<style scoped>
.con {
  width: 1400px;
  border: 1px solid red;
  /* height: 100vh; */
  background: #ffffff;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.item {
  width: 260px;
  height: 450px;
  background: #ffffff;
  box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  margin-bottom: 25px;
}
.item img {
  width: 260px;
  height: 260px;
  background: #ffffff;
  border-radius: 4px 0px 0px 4px;
  display: block;
}
.item .name span {
  width: 91px;
  height: 27px;
  font-size: 24px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  line-height: 28px;
}
.item .name .vip {
  width: 36px;
  height: 18px;
  margin: 5px 0 0 12px;
}
.item .name .hot {
  width: 16px;
  height: 18px;
  margin: 5px 0 0 10px;
}
</style>
