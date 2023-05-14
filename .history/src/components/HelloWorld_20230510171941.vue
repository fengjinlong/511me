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
          I am very caring and responsible, and I love children very
          muchmuchmuch. I am
        </div>
        <div class="f4">
          <div>
            <img src="./like2.png" alt="" />
            <span>Like</span>
          </div>
          <div>
            <img src="./hi.png" alt="" />
            <span>Message</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const list = [1, 2, 3, 4, 5, , 1, 1, 1, 1];
</script>
<style scoped></style>
