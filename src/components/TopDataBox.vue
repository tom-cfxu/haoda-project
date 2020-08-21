<template>
  <div id="topBox">
    <div class="top-data-box" v-for="item in data" :key="item.id">
      <p class="title">{{item.title}}</p>
      <p class="value">{{item.value}}</p>
      <img class="icon" :src="require(`../assets/images/top/top_icon_${item.icon}.png`)" />
    </div>
  </div>
</template>

<script>
export default {
  name: "TopDataBox",

  props: {
    data: Array,
  },
  created() {
    // console.log(this.data);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
@font-face {
  /*font-properties*/
  font-family: Nasa Display;
  src: url("../assets/font/液晶4.ttf");
}
#topBox {
  display: flex;
}
.top-data-box {
  //   height: 100%;
  width: 482/2.5px;
  height: 144/2px;
  background-image: url("../assets/images/top/top_kuang_bg.png");
  background-size: contain;
  background-repeat: no-repeat;
  margin: 10px 5px;
  position: relative;
}
.title {
  position: relative;
  top: 5px;
  left: -50px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
}
.value {
  position: relative;
  color: #f09c03;
  letter-spacing: 5px;
  font-family: Nasa Display;
  bottom: -2px;
  left: 0px;
  width: 100%;
  font-size: 36px;
  text-align: center;
}
.icon {
  position: absolute;
  top: -5px;
  right: -5px;
  width: 86/2px;
  height: 86/2px;
}
</style>
