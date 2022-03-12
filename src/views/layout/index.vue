<template>
  <div class="layout">
    <van-row type="flex" justify="end" class="top-logo">
      <van-col span="14">
        <van-cell value="全国最大的电动车交易平台"/>
      </van-col>
      <van-col span="10" id="caidan-buttun">
        <van-button icon="search" plain  type="info" size="small" to="/search">搜索</van-button>
      </van-col>
    </van-row>
    <Home id="home"></Home>
    <van-tabbar v-model="active">
      <van-tabbar-item icon="home-o">首页</van-tabbar-item>
      <van-tabbar-item icon="search" to="/search">搜索</van-tabbar-item>
      <van-tabbar-item icon="guide-o" to="/search">城市</van-tabbar-item>
      <van-tabbar-item icon="user-o" to="/login">登录</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
// @ is an alias to /src
import Home from '../home/index.vue'
export default {
  name: 'Layout',
  components: {
    Home
  },
  data () {
    return {
      active: 0,
      icon: {
        active: 'https://img01.yzcdn.cn/vant/user-active.png',
        inactive: 'https://img01.yzcdn.cn/vant/user-inactive.png'
      }
    }
  }
}
</script>

<style lang="scss" >
.layout{
  height: 100%;
  .top-logo{
    width: 100%;
    position: fixed;
    z-index: 99;
    background-color: #fff;
  }
  #caidan-buttun{
    display: flex;
    justify-content: right ;
    align-items: center;
    .van-button{
      margin-right: 10px;
    }
  }
}
</style>
