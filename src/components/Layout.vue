<template>
  <van-config-provider :theme="theme">
    <div :class="theme" class="layout-container">
      <!-- Nội dung chính -->
      <router-view style="margin: 30px 0 150px 0;" @update-theme="setTheme" />

      <!-- Tabbar điều hướng -->
      <van-tabbar route>
        <van-tabbar-item replace to="/Profile" icon="home-o">Home</van-tabbar-item>
        <van-tabbar-item replace to="/Action" icon="search">Search</van-tabbar-item>
        <van-tabbar-item replace to="/Setting" icon="setting-o">Setting</van-tabbar-item>
      </van-tabbar>
    </div>

  </van-config-provider>
</template>

<script>
export default {
  name: "LayoutPage",
  data() {
    return {
      theme: localStorage.getItem("theme") || "light", // Lấy theme từ localStorage hoặc mặc định là light
    };
  },
  methods: {
    setTheme(newTheme) {
      this.theme = newTheme;
      localStorage.setItem("theme", newTheme); // Lưu vào localStorage
      document.documentElement.setAttribute("data-theme", newTheme); // Cập nhật class trên toàn bộ HTML
    },
  },
  mounted() {
    // Áp dụng theme khi tải trang
    document.documentElement.setAttribute("data-theme", this.theme);
  },
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