<template>
<van-config-provider :theme="theme">
  <van-switch v-model="checked"  active-color="#dcdee0" inactive-color="#000">
  <template #node>
    <div class="icon-wrapper">
      <van-icon :name="checked ? 'success' : 'cross'" />
    </div>
  </template>
</van-switch>
<van-divider></van-divider>
<audio ref="backgroundMusic" :src="musicSrc" autoplay loop></audio>
<img src="@/assets/biu.jpg" alt="">
<van-highlight :keywords="keywords" source-string="Trang đang được phát triển, vì vậy hãy chú ý theo dõi" />
</van-config-provider>

</template>

<script>
export default {
  name: "SettingPage",
  data(){
    return{
      checked: true,
      theme: "light",
      musicSrc: require("../assets/music.mp3")
    }
  },
  watch: {
    checked(newVal) {
      this.theme = newVal ? "light" : "dark";
    },
  },
};
</script>

<style scoped>

  .icon-wrapper {
    display: flex;
    width: 100%;
    justify-content: center;
    font-size: 18px;
  }

  .icon-wrapper .van-icon-success {
    line-height: 32px;
    color: var(--van-blue);
  }

  .icon-wrapper .van-icon-cross {
    line-height: 32px;
    color: var(--van-gray-5);
  }
 
</style>