<template>
  <div>
    <div class="list">
      <img class="img1" src="./1.png" />
      <div class="font">
        <div class="name">
          <span>name</span>
          <img class="vip" src="./vip1.png" />
        </div>
        <div class="price">price</div>
        <div class="sale">sale</div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.list {
  width: 100%;
  height: 228px;
}
.list .img1 {
  flex: 0 0 228px;
  height: 228px;
}
.list .font {
  flex: 1;
}
</style>
