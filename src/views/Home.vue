<template>
  <div id="home">
    <!-- 顶部 -->
    <div class="top">
      <!-- 顶部左边三个 -->
      <TopDataBox v-bind:data="topDataLeft" />
      <!-- 顶部中间 -->
      <TopCenterBox />
      <!-- 顶部右边三个 -->
      <TopDataBox v-bind:data="topDataRight" />
    </div>
    <!-- 内容 -->
    <div class="container">
      <!-- 内容-左部 -->
      <div class="left">
        <ContainerBox>你好</ContainerBox>
      </div>
      <!-- 内容-中间 -->
      <div class="center"></div>
      <!-- 内容-右边 -->
      <div class="right"></div>
    </div>
    <!-- 尾部 -->
    <div class="footer"></div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import TopDataBox from "@/components/TopDataBox.vue";
import TopCenterBox from "@/components/TopCenterBox.vue";
import ContainerBox from "@/components/ContainerBox.vue";
export default {
  name: "Home",
  data() {
    return {
      topDataLeft: [
        {
          id: 0,
          title: "服务设备总数",
          value: "87580",
          icon: "fwzbzs",
        },
        {
          id: 1,
          title: "服务单位总数",
          value: "246",
          icon: "bzdwzs",
        },
        {
          id: 2,
          title: "服务人员总数",
          value: "4692",
          icon: "bzryzs",
        },
      ],
      topDataRight: [
        {
          id: 0,
          title: "客户总数",
          value: "853",
          icon: "bzryzs",
        },
        {
          id: 1,
          title: "需求总数",
          value: "7486",
          icon: "bzxqzs",
        },
        {
          id: 2,
          title: "任务书",
          value: "87580",
          icon: "bzrwzs",
        },
      ],
    };
  },
  components: {
    // HelloWorld
    TopDataBox,
    TopCenterBox,
    ContainerBox,
  },
};
</script>
<style lang="less" >
body {
  background-color: #05122d;
  background-image: url("../assets/images/bg.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  height: 100vh;
}
#home {
  position: relative;
}
.top {
  display: flex;
  justify-content: space-evenly;
}
.container {
  position: relative;
  top: -15px;
  display: flex;
  // justify-content: space-evenly;
  align-items: center;
}
</style>