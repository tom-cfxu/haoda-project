<template>
  <div id="centerDivBox">
    <p class="title">
      <img class="icon" src="../assets/images/bgzygl_icon_beijinan.png" />
      <span>运维设备统计</span>
    </p>

    <slot class="container"></slot>
  </div>
</template>

<script>
export default {
  name: "ContainerBox",

  props: {
    data: Array,
  },
  methods: {
    setWH(id) {
      let dom = document.getElementById(id);
      console.log(dom);
      // dom.style.backgroundImage = "url('../assets/images/bg_zuo1.png')";
      var img = new Image();
      dom.classList.add("bg1");
      img.src = "../assets/images/bg_zuo1.png";
      // img.width
      // console.log(img.width);
    },
  },
  created() {},
  mounted() {
    this.setWH("centerDivBox");
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
img {
  max-width: 100%;
  height: auto;
}
#centerDivBox {
  width: 833/2px;
  height: 438/2px;
  background-size: contain;
  background-repeat: no-repeat;
  margin: 10px;
}
.bg1 {
  background-image: url(../assets/images/bg_zuo1.png);
}
.title {
  display: flex;
  padding: 5px;
  width: 200px;
  // margin-top: 5px;
  position: relative;
  top: 2px;
  margin-left: 15px;
  span {
    display: inline-block;
    margin-left: 5px;
  }
}
.icon {
  width: 39/2px;
  height: 33/2px;
  margin-top: 4px;
  display: inline-block;
}
</style>
