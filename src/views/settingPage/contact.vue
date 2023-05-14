<template>
  <div class="notify">
    <p class="p1">Is it urgent?</p>
    <p class="p2">
      Feel free to send us email at yueyuankeji@163.com. Our friendly customer
      service agents will respond within 24 hours on weekdays.
    </p>
  </div>
</template>
<script setup>
import { ref } from "vue";
const input = ref("");
</script>
<style lang="scss" scoped>
.notify {
  width: 100%;
  .p1 {
    width: 223px;
    height: 25px;
    font-size: 22px;
    font-family: Arial-BoldMT, Arial;
    font-weight: normal;
    color: #000000;
    line-height: 26px;
    padding-top: 25px;
    padding-left: 40px;
  }
  .p2 {
    width: 893px;
    height: 22px;
    font-size: 22px;
    font-family: ArialMT;
    color: #666666;
    line-height: 22px;
    padding: 20px 0 40px 40px;
  }
}
</style>
