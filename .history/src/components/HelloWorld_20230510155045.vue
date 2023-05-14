<template>
  <div class="con">
    <div v-for="ele of list" class="item">1</div>
  </div>
</template>
<script setup>
const list = [1, 2, 3, 4, 5, , 1, 1, 1, 1];
</script>
<style scoped>
.con {
  width: 1400px;
  border: 1px solid red;
  height: 100vh;
  background: #ffffff;
}
.item {
  width: 260px;
  height: 260px;
}
</style>
