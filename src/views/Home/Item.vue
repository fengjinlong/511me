<template>
  <div class="item" @click="jump">
    <img src="../../assets/home/1.png" alt="" />
    <div class="font">
      <div class="name">
        <span>Jerry,29</span>
        <img class="vip" src="../../assets/home/vip1.png" alt="" />
        <img class="hot" src="../../assets/home/hot.png" alt="" />
      </div>
      <div class="f1">Earns&nbsp;$&nbsp;30000-&nbsp;$&nbsp;45000</div>
      <div class="f1">Living&nbsp;in&nbsp;China-beijing</div>
      <div class="f3">
        I am very caring and responsible, and I love children very muchmuchmuch.
        I am
      </div>
      <div class="f4">
        <div>
          <img src="../../assets/home/like2.png" alt="" />
          <span>Like</span>
        </div>
        <div>
          <img src="../../assets/home/hi.png" alt="" />
          <span>Message</span>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
// import { useRouter } from "vue-router";
// const router = useRouter();
// const p = defineProps({
//   ele: Number,
// });

const jump = () => {
  // router.push({
  //   path: "details",
  //   params: {
  //     id: p.ele,
  //   },
  // });
};
</script>
<style scoped>
.item {
  width: 146px;
  height: 253px;
  background: #ffffff;
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  margin-bottom: 14px;
}
.item img {
  width: 146px;
  height: 146px;
  background: #ffffff;
  display: block;
}
.item .font {
  padding: 5px 7px 8px;
}
.item .font .name {
  height: 15px;
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  font-family: Arial-BoldMT;
  text-align: left;
  white-space: nowrap;
  display: flex;
}
.item .font .name span {
  height: 15px;
  font-size: 14px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  line-height: 16px;
}
.item .font .name .vip {
  width: 20px;
  height: 10px;
  margin: 3px 0 0 7px;
}
.item .font .name .hot {
  width: 9px;
  height: 10px;
  margin: 3px 0 0 6px;
}
.item .font .f1 {
  height: 10px;
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  font-size: 9px;
  font-family: ArialMT;
  text-align: left;
  white-space: nowrap;
  line-height: 10px;
  margin: 5px 0 0 0;
}
.item .font .f3 {
  /* height: 23px; */
  overflow-wrap: break-word;
  font-size: 8px;
  zoom: 0.83;
  font-family: ArialMT;
  text-align: left;
  line-height: 13px;
  margin: 6px 0 0 0;
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
  margin-top: 5px;
}
.item .font .f4 div {
  border-radius: 2px;
  width: 61px;
  height: 18px;
  border: 1px solid rgba(182, 0, 56, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.item .font .f4 div img {
  width: 12px;
  height: 11px;
  margin-right: 7px;
}
.item .font .f4 div span {
  font-size: 8px;
  color: #b60038;
  line-height: 9px;
  zoom: 0.67;
}
</style>
