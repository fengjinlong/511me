<template>
  <div class="item" @click="jump">
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
        I am very caring and responsible, and I love children very muchmuchmuch.
        I am
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
</template>
<script setup>
const p = defineProps({
  ele: Numberr,
});

console.log("ele", p);
const jump = () => {
  console.log("jump");
};
</script>
<style scoped>
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
  text-align: left;
  white-space: nowrap;
  line-height: 18px;
  margin: 8px 0 0 0;
}
.item .font .f3 {
  height: 40px;
  overflow-wrap: break-word;
  font-size: 14px;
  font-family: ArialMT;
  text-align: left;
  line-height: 20px;
  margin: 8px 0 0 0;
  color: #666;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}
.item .font .f4 {
  display: flex;
  justify-content: space-between;
  margin-top: 9px;
}
.item .font .f4 div {
  border-radius: 3px;
  width: 112px;
  height: 32px;
  border: 1px solid rgba(182, 0, 56, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.item .font .f4 div img {
  width: 21px;
  height: 19px;
  margin-right: 10px;
}
.item .font .f4 div span {
  font-size: 14px;
  color: #b60038;
  line-height: 16px;
}
</style>
