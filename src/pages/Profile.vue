<template>
  <div class="content">
    <div class="header_content">
      <van-image
        round
        fit=cover
        width="10rem"
        height="10rem"
        :src="require('@/assets/avt.jpg')"
      />
      <br>
      <van-highlight :keywords="keywords" source-string="Mình là Nguyễn Dương, Chào mừng bạn đến với website của mình" />
    </div>
    <div class="section_content">
      <van-row justify="center">
        <van-col span="24">
          <van-button color="linear-gradient(to right, #ff6034, #ee0a24)" type="primary" size="large" url="https://www.facebook.com/duongitbg01">Facebook</van-button>
        </van-col>
      </van-row>
      <van-row justify="center">
        <van-col span="24">
          <van-button color="linear-gradient(to right, #ff6034, #ee0a24)" type="primary" size="large" url="https://www.instagram.com/duongbg01">Instagram</van-button>
        </van-col>
      </van-row>
      <van-row justify="center">
        <van-col span="24">
          <van-button color="linear-gradient(to right, #ff6034, #ee0a24)" type="primary" size="large" url="https://youtu.be/f0gi7UG1L0w">Youtube</van-button>
        </van-col>
      </van-row>
      <van-row justify="center">
        <van-col span="24">
          <van-button color="linear-gradient(to right, #ff6034, #ee0a24)" type="primary" size="large" url="nguyenvanduongit01@gmail.com">Gmail</van-button>
        </van-col>
      </van-row>
      <van-row justify="center">
        <van-col span="24">
          <van-button color="linear-gradient(to right, #ff6034, #ee0a24)" type="primary" size="large" url="https://github.com/Duong01/Duong01">Github</van-button>
        </van-col>
      </van-row>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "ProfilePage",
  data(){
    return{
      
    }
  }
};
</script>

<style scoped>
.van-row {
  padding: 30px 0;
}
.notice-swipe {
    height: 40px;
    line-height: 40px;
  }
</style>