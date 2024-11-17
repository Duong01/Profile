<template>
  <router-view style="margin: 30px 0 150px 0;"  />
  <!-- <van-config-provider theme="dark"> -->
  <van-tabbar route >
    <van-tabbar-item replace to="/Profile" icon="home-o">Home</van-tabbar-item>
    <van-tabbar-item replace to="/Action" icon="search">Search</van-tabbar-item>
    
    <!-- <van-tabbar-item replace to="" icon="friends-o">Tab 3</van-tabbar-item> -->
    <van-tabbar-item replace to="/Setting" icon="setting-o">Setting</van-tabbar-item>
  </van-tabbar>
<!-- </van-config-provider> -->
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
.van-tabbar-item {
  margin-bottom: 10px;
}
.van-tabbar--fixed {
    position: fixed;
    height: 70px;
    bottom: 0;
    left: 0;
}
</style>