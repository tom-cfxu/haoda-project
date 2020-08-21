<template>
  <div id="topCenterBox">
    <div class="topCenterBox">
      <p class="title">某设备运维管理平台</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopCenterBox",

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
.topCenterBox {
  width: 1203/2px;
  height: 165/2px;
  background-image: url(../assets/images/top/top_name.png);
  background-size: contain;
  background-repeat: no-repeat;
  margin: 10px;
  position: relative;
  flex: 1;
}
.title {
  position: absolute;
  top: 10px;
  left: 138px;
  font-weight: 400;
  font-size: 36px;
  margin: 0;
  padding: 0;
}
</style>
