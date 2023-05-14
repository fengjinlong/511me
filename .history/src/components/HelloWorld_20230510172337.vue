<template>
  <div class="con">
    <Item :ele="ele" v-for="ele of list" :key="ele" />
  </div>
</template>
<script setup>
import Item from "./Item.vue";
const list = [1, 2, 3, 4, 5, , 1, 1, 1, 1];
</script>
<style scoped>
.con {
  width: 1400px;
  background: #ffffff;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 0 auto;
}
</style>
