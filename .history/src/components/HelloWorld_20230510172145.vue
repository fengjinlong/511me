<template>
  <div class="con">
    <Item v-for="ele of list" />
  </div>
</template>
<script setup>
import Item from "./Item.vue";
const list = [1, 2, 3, 4, 5, , 1, 1, 1, 1];
</script>
<style scoped></style>
