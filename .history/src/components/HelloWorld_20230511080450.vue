<template>
  <div class="con">
    <Item :ele="ele" v-for="ele of list" :key="ele" />
    <div>
      <div class="item">
        <img
          src="https://img.alicdn.com/imgextra/i1/O1CN01QYQY2e1CZQYQY2e1C_!!6000000000000-2-tps-260-260.png"
        />
        <div class="font">
          <div class="name">
            <span>name</span>
            <img
              class="vip"
              src="https://img.alicdn.com/imgextra/i1/O1CN01QYQY2e1CZQYQY2e1C_!!6000000000000-2-tps-260-260.png"
            />
          </div>
          <div class="price">price</div>
          <div class="sale">sale</div>
        </div>
      </div>
    </div>
  </div>
  <button @click="add">add</button>
</template>
<script setup>
import { reactive } from "vue";
import Item from "./Item.vue";
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
