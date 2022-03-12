<template>
  <div class="home">
    <van-swipe class="my-swipe" :autoplay="3000" indicator-color="white" >
      <van-swipe-item>广告区域1</van-swipe-item>
      <van-swipe-item>
        <img src="https://img01.yzcdn.cn/vant/apple-1.jpg" alt="">
      </van-swipe-item>
      <van-swipe-item>
        <img src="https://img01.yzcdn.cn/vant/apple-1.jpg" alt="">
      </van-swipe-item>
      <van-swipe-item>广告区域4</van-swipe-item>
    </van-swipe>
    <div class="shopping">
    <van-card
      num="2"
      tag="标签"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      origin-price="10.00"
    />
    <van-card
      num="2"
      tag="标签"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      origin-price="10.00"
    />
    <van-card
      num="2"
      tag="标签"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      origin-price="10.00"
    />
    <van-card
      num="2"
      tag="标签"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      origin-price="10.00"
    />
    <van-card
      num="2"
      tag="标签"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      origin-price="10.00"
    />
    </div>

  </div>
</template>

<script>
import { Toast } from 'vant'
export default {
  name: 'Home',
  data () {
    return {
      images: [
        'https://img01.yzcdn.cn/vant/apple-1.jpg',
        'https://img01.yzcdn.cn/vant/apple-2.jpg'
      ]
    }
  },
  methods: {
    onChange (index) {
      Toast('当前 Swipe 索引：' + index)
    }
  }
}
</script>

<style lang="scss">
.home{
  width: 100%;
  height: 100%;
  background-color: rgb(74, 149, 211);
  .banner{
    height: 200px;
  }
   .my-swipe .van-swipe-item {
    width: 100%;
    height: 150px;
    color: #fff;
    font-size: 20px;
    line-height: 150px;
    text-align: center;
    background-color: #39a9ed;
    img{
    width: 100%;
    height: 150px;
    }
  }
  .my-swipe{
    position: fixed;
    z-index: 99;
    top: 50px;
  }
  .shopping{
    padding-top: 210px;
    padding-bottom: 50px;
  }
}
</style>
