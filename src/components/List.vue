<template>
  <div>
    <div class="item">
      <img class="img1" src="./1.png" />
      <div class="font">
        <div class="name">
          <span>Jerry,29</span>
          <img class="vip" src="./vip1.png" alt="" />
          <img class="hot" src="./hot.png" alt="" />
        </div>
        <div class="f1">Female / ID: 1729063</div>
        <div class="f1 f2">Earns $ 30000- $ 450 Earns $ 30000- $ 450</div>
        <div class="f3">
          I am 48 years old and 162cm tall in Beijing. I am in a relationship
          for the purpose of getting married, and I am looking for a date to
          return to China
        </div>
      </div>
      <div class="f4">
        <div>
          <img src="./like2.png" alt="" />
          <span>Like</span>
        </div>
        <div>
          <img class="hi" src="./hi.png" alt="" />
          <span>Message</span>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.item {
  width: 100%;
  height: 228px;
  display: flex;
  margin-bottom: 34px;
  position: relative;
}
.item .img1 {
  flex: 0 0 228px;
  height: 228px;
}
.item .font {
  flex: 1;
  padding-left: 50px;
}
.item .font .name {
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  font-size: 24px;
  font-family: Arial-BoldMT;
  font-weight: NaN;
  text-align: left;
  white-space: nowrap;
  line-height: 28px;
  display: flex;
  margin-bottom: 20px;
  align-items: center;
}
.item .font .name span {
  font-size: 36px;
  font-family: Arial-BoldMT, Arial;
  font-weight: normal;
  color: #000000;
  height: 41px;
  line-height: 42px;
}
.item .font .name .vip {
  width: 44px;
  height: 22px;
  margin: 0 0 0 16px;
}
.item .font .name .hot {
  width: 19px;
  height: 22px;
  margin: 0 0 0 12px;
}
.item .font .f1 {
  overflow-wrap: break-word;
  color: rgba(0, 0, 0, 1);
  text-align: left;
  white-space: nowrap;
  margin-bottom: 20px;
  font-size: 24px;
  font-family: ArialMT;
  color: #999999;
  line-height: 28px;
}
.item .font .f1.f2 {
  margin-bottom: 17px;
}
.item .font .f3 {
  color: #666;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;

  font-size: 24px;
  font-family: PingFangSC-Regular, PingFang SC;
  font-weight: 400;
  height: 80px;
  line-height: 38px;
}
.item .f4 {
  position: absolute;
  top: 0;
  right: 0;
}
.item .f4 div {
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  width: 168px;
  height: 48px;
  background: #ffffff;
  border-radius: 5px;
  border: 2px solid #b60038;
  margin-bottom: 20px;
}
.item .f4 div img {
  width: 32px;
  height: 29px;
  margin-right: 18px;
}
.item .f4 div img.hi {
  width: 31px;
  height: 30px;
}
.item .f4 div span {
  font-size: 21px;
  font-family: ArialMT;
  color: #b60038;
  line-height: 24px;
}
</style>
