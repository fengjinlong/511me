<template>
  <div :class="{ item: true, border: ele === 2 ? true : false }">
    <img
      v-show="ele === 2"
      class="sel"
      src="../../assets/home/Selected.png"
      alt=""
    />
    <img
      class="img"
      src="../../assets/home/1.png"
      alt=""
      @click="jump(ele.userid)"
    />
    <div class="font">
      <div class="name">
        <span>asdfasd</span>
        <img class="vip" src="../../assets/home/vip1.png" alt="" />

        <img class="hot" src="../../assets/home/hot.png" alt="" />
      </div>
      <!-- <div class="f1">Earns&nbsp;$&nbsp;30000-&nbsp;$&nbsp;45000</div> -->
      <div class="f1">Earns $ 75000- $ 150000</div>
      <div class="f1">Living in China-shanghai</div>
      <div class="f3">
        I am very caring and responsiblesib,siband I lsib sibove children very
        much. I am
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
// import router from "@/router";
const p = defineProps({
  ele: Object,
});

const ele = ref(p.ele);
const add = (like, touserid) => {
  // if (like === 1) return;
  // addLove({ touserid }).then((res) => {
  //   if (res.code === "200") {
  //     ele.value.like = 1;
  //   }
  // });
};
const jump = (touserid) => {
  router.push({
    path: `/details/${touserid}`,
  });
};
</script>
<style scoped>
.item {
  margin-bottom: 14px;

  width: 234px;
  height: 394px;
  background: #ffffff;

  border-radius: 4px;
  border: 3px solid transparent;
  position: relative;
}
.item .sel {
  position: absolute;
  top: 0;
  right: 0;
  width: 50px;
  height: 50px;
}
.item.border {
  box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.15);
  border-color: #b60038;
}
.item .img {
  width: 234px;
  height: 234px;
  background: #ffffff;
  display: block;
}
.item .font {
  padding: 8px 0 7px 11px;
}
.item .font .name {
  text-align: left;
  display: flex;

  height: 25px;
  font-size: 22px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  line-height: 26px;
}
.item .font .name span {
  height: 25px;
  font-size: 22px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  line-height: 26px;
}
.item .font .name .vip {
  width: 32px;
  height: 16px;
  margin: 0 0 0 13px;
}
.item .font .name .hot {
  width: 14px;
  height: 16px;
  margin: 0 0 0 9px;
}
.item .font .f1 {
  text-align: left;
  white-space: nowrap;
  margin: 7px 0 0 0;
  height: 20px;
  font-size: 18px;
  font-family: ArialMT;
  color: #000000;
  line-height: 21px;
}
.item .font .f3 {
  overflow-wrap: break-word;
  text-align: left;
  margin: 6px 0 0 0;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;

  height: 54px;
  font-size: 16px;
  font-family: ArialMT;
  color: #666666;
  line-height: 18px;
}
</style>
