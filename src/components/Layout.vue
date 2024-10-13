<template>
  <van-config-provider theme="dark">
  <van-tabbar route fixed style="position: fixed; top: 0; left: 0; right: 0; z-index: 10;">
    <van-tabbar-item replace to="/Profile" icon="home-o">Home</van-tabbar-item>
    <van-tabbar-item replace to="/Action" icon="search">Tab</van-tabbar-item>
    
    <!-- <van-tabbar-item replace to="" icon="friends-o">Tab 3</van-tabbar-item> -->
    <van-tabbar-item replace to="/Setting" icon="setting-o">Tab 4</van-tabbar-item>
  </van-tabbar>
  <router-view style="margin-top: 70px;"  />
</van-config-provider>
</template>

<script>
export default {
  name: "LayoutPage"
};
</script>

<style>
.van-button--primary {
  color: var(--van-button-primary-color);
  background-color: var(--van-button-primary-background);
}
:root {
  --van-white: #fff;
  --van-blue: #1989fa;
  --van-button-primary-color: var(--van-white);
  --van-button-primary-background: var(--van-primary-color);
}
.van-theme-dark body {
  color: #fff;
  background-color: black;
}
</style>