<template>
  <div class="con">
    <div v-for="ele of list" :key="ele" class="item">
      <img src="./1.png" alt="" />
      <div class="name">
        <span></span>
        <img src="" alt="" />
        <img src="" alt="" />
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
</style>
