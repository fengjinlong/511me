<template>
  <!-- <div class="item blur"> -->
  <div class="item">
    <img class="img1" src="../../assets/home/1.png" />
    <div class="font">
      <div class="name">
        <span>Jerry,29</span>
        <img class="vip" src="../../assets/home/vip1.png" alt="" />
        <img class="hot" src="../../assets/home/hot.png" alt="" />
      </div>
      <div class="f1">Female / ID: 1729063</div>
      <div class="f1 f2">Earns $ 30000- $ 450 Earns $ 30000- $ 450</div>
      <div class="f3">
        I am 48 years old and 162cm tall in Beijing. I am in a relationship for
        the purpose of getting married, and I am looking for a date to return to
        China
      </div>
    </div>
    <div class="f4">
      <div>
        <img src="../../assets/home/like2.png" alt="" />
        <span>Like</span>
      </div>
      <div>
        <img class="hi" src="../../assets/home/hi.png" alt="" />
        <span>Message</span>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.item {
  width: 100%;
  height: 128px;
  display: flex;
  margin-bottom: 19px;
  position: relative;

  .img1 {
    flex: 0 0 128px;
    height: 128px;
  }
  .font {
    flex: 1;
    padding-left: 50px;
    .name {
      overflow-wrap: break-word;
      color: rgba(0, 0, 0, 1);
      font-size: 24px;
      font-family: Arial-BoldMT;
      font-weight: NaN;
      text-align: left;
      white-space: nowrap;
      line-height: 28px;
      display: flex;
      margin-bottom: 11px;
      align-items: center;
      span {
        font-size: 20px;
        font-family: Arial-BoldMT, Arial;
        font-weight: normal;
        color: #000000;
        line-height: 24px;
      }
      .vip {
        width: 25px;
        height: 15px;
        margin: 0 0 0 9px;
      }
      .hot {
        width: 11px;
        height: 12px;
        margin: 0 0 0 7px;
      }
    }
    .f1 {
      overflow-wrap: break-word;
      text-align: left;
      white-space: nowrap;
      margin-bottom: 11px;

      font-size: 14px;
      font-family: ArialMT;
      color: #999999;
      line-height: 16px;
    }
    .f3 {
      color: #666;
      overflow: hidden;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-box-orient: vertical;
      -webkit-line-clamp: 2;

      height: 45px;
      font-size: 14px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: #666666;
      line-height: 21px;
    }
    .f1.f2 {
      margin-bottom: 10px;
    }
  }
}
.blur {
  filter: blur(7px);
}
.item .f4 {
  position: absolute;
  top: 0;
  right: 0;
  div {
    width: 95px;
    height: 25px;
    background: #ffffff;
    border-radius: 3px;
    border: 1px solid #b60038;

    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    margin-bottom: 11px;
    img {
      width: 18px;
      height: 16px;
      margin-right: 18px;
    }
    img.hi {
      width: 17px;
      height: 17px;
    }
    span {
      font-family: ArialMT;
      color: #b60038;
      font-size: 12px;
      line-height: 14px;
    }
  }
}
</style>
