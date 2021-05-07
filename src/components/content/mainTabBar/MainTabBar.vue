<template>
  <tab-bar>
    <!--      常量不需要加上v-bind-->
    <tab-bar-item path="/home" activeColor="deeppink">
      <img slot="item-icon" src="assets/img/tabbar/001.jpg">
      <img slot="item-icon-active" src="../../assets/img/tabbar/04.jpg">
      <!--        <img slot="item-icon-active" src="./assets/img/tabbar/001.jpg.jpg">-->

      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="deeppink">
      <img slot="item-icon" src="../../assets/img/tabbar/001.jpg">
      <img slot="item-icon-active" src="../../assets/img/tabbar/04.jpg">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="deeppink">
      <img slot="item-icon" src="../../assets/img/tabbar/001.jpg">
      <img slot="item-icon-active" src="../../assets/img/tabbar/04.jpg">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="deeppink">
      <img slot="item-icon" src="../../assets/img/tabbar/001.jpg">
      <img slot="item-icon-active" src="../../assets/img/tabbar/04.jpg">
      <div slot="item-text">首页</div>
    </tab-bar-item>
  </tab-bar>
</template>
<script>
  import TabBar from "../tabbar/Tabbar";
  import TabBarItem from "../tabbar/TabBarItem";
    export default {
        name: "MainTabBar",
      components:{
        TabBar,
        TabBarItem
      }
    }
</script>

<style scoped>

</style>
