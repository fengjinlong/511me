<template>
  <div class="con">
    <div v-for="ele of list" :key="ele" class="item">
      <img src="./1.png" alt="" />
      <div class="font">
        <div class="name">
          <span>Jerry,29</span>
          <img class="vip" src="./vip1.png" alt="" />
          <img class="hot" src="./hot.png" alt="" />
        </div>
        <div class="f1">Earns&nbsp;$&nbsp;30000-&nbsp;$&nbsp;45000</div>
        <div class="f1">Living&nbsp;in&nbsp;China-beijing</div>
        <div class="f3">
          I am very caring and I am very caring and I am very caring and
        </div>
        <div class="f4"></div>
      </div>
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
.item .font {
  padding: 9px 12px 15px;
}
.item .font .name {
  height: 27px;
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  font-size: 24px;
  font-family: Arial-BoldMT;
  font-weight: NaN;
  text-align: left;
  white-space: nowrap;
  line-height: 28px;
  display: flex;
}
.item .font .name span {
  width: 91px;
  height: 27px;
  font-size: 24px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  line-height: 28px;
}
.item .font .name .vip {
  width: 36px;
  height: 18px;
  margin: 5px 0 0 12px;
}
.item .font .name .hot {
  width: 16px;
  height: 18px;
  margin: 5px 0 0 10px;
}
.item .font .f1 {
  height: 17px;
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  font-size: 16px;
  font-family: ArialMT;
  font-weight: NaN;
  text-align: left;
  white-space: nowrap;
  line-height: 18px;
  margin: 8px 0 0 12px;
}
.item .font .f3 {
  height: 40px;
  overflow-wrap: break-word;
  font-size: 0;
  font-family: ArialMT;
  font-weight: NaN;
  text-align: left;
  line-height: 20px;
  margin: 8px 0 0 12px;
}
</style>
