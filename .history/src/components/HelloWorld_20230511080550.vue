<template>
  <div class="con">
    <Item :ele="ele" v-for="ele of list" :key="ele" />
    <list />
  </div>
  <button @click="add">add</button>
</template>
<script setup>
import { reactive } from "vue";
import Item from "./Item.vue";
import List from "./List.vue";
const list = reactive([1, 2]);
const add = () => {
  list.push(1);
};
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
