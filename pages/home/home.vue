<template>
  <view class="content">
    <uni-nav-bar :fixed="true" :border="false">
      <block slot="left">
        <view class="city">
          <view>
            <text class="uni-nav-bar-text">{{ city }}</text>
          </view>
          <uni-icons type="arrowdown" color="#666" size="18" />
        </view>
      </block>
      <view class="input-view">
        <uni-icons class="input-uni-icon" type="search" size="18" color="#999" />
        <input confirm-type="search" class="nav-bar-input" type="text" placeholder="输入搜索关键词"
          @confirm="confirm" />
      </view>
      <block slot="right">
        <view class="city">
          搜索
        </view>
      </block>
    </uni-nav-bar>

    <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
      <swiper-item>
        <image
          src="https://img.zcool.cn/community/011fbd58ec3c55a8012049ef034bbc.jpg@3000w_1l_2o_100sh.jpg"
          mode=""></image>
      </swiper-item>
      <swiper-item>
        <image
          src="https://img.zcool.cn/community/011fbd58ec3c55a8012049ef034bbc.jpg@3000w_1l_2o_100sh.jpg"
          mode=""></image>
      </swiper-item>
    </swiper>

    <view class="cateBox">
      <view class="c-item">
        <image
          src="https://images.pexels.com/photos/8396730/pexels-photo-8396730.jpeg?auto=compress&cs=tinysrgb&w=600"
          mode=""></image>
        <view class="tit">
          潮流
        </view>
      </view>
      <view class="c-item">
        <image
          src="https://images.pexels.com/photos/8400603/pexels-photo-8400603.jpeg?auto=compress&cs=tinysrgb&w=600"
          mode=""></image>
        <view class="tit">
          复古
        </view>
      </view>
      <view class="c-item">
        <image
          src="https://images.pexels.com/photos/8386653/pexels-photo-8386653.jpeg?auto=compress&cs=tinysrgb&w=600"
          mode=""></image>
        <view class="tit">
          最新
        </view>
      </view>
      <view class="c-item">
        <image
          src="https://images.pexels.com/photos/8581058/pexels-photo-8581058.jpeg?auto=compress&cs=tinysrgb&w=600"
          mode=""></image>
        <view class="tit">
          其他
        </view>
      </view>
    </view>

    <scroll-view :scroll-x="true" class="scrollview-box">
      <block v-for="(item,index) in scrollList" :key="index">
        <view class="item">
          <image :src="item.img" mode="aspectFill"></image>
          <view class="tit">
            <view>{{item.name}}</view>
            <view style="color: darkred;">￥{{item.price}}</view>
          </view>
        </view>
      </block>
    </scroll-view>


    <view class="box">
      <view class="title">
        推荐商品
      </view>

      <view class="lists">
        <view class="h-item" v-for="(item,index) in scrollList.slice(0,3)" :key="index">
          <view class="left">
            <image :src="item.img" mode="aspectFill"></image>
          </view>
          <view class="info">
            <view class="tit">
              {{item.name}}
            </view>
            <view class="auther">
              价格: ￥{{item.price}}
            </view>
          </view>
          <view class="icons">
            流行
          </view>
        </view>
      </view>
    </view>

    <view class="box">
      <view class="title">
        热门商品
      </view>

      <view class="lists-two">
        <view class="item" v-for="(item,index) in scrollList.slice(0,4)" :key="index">
          <image :src="item.img" mode="aspectFill"></image>
          <view class="title fx">
            <view>{{item.name}}</view>
            <view style="color: darkred; font-weight: 500;">￥{{item.price}}</view>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        city: '北京',
        cateList: [],
        scrollList: [{
            img: 'https://images.pexels.com/photos/9594679/pexels-photo-9594679.jpeg?auto=compress&cs=tinysrgb&w=600',
            name: '潮流服装',
            price: '99.00'
          },
          {
            img: 'https://images.pexels.com/photos/9594679/pexels-photo-9594679.jpeg?auto=compress&cs=tinysrgb&w=600',
            name: '潮流服装',
            price: '99.00'
          },
          {
            img: 'https://images.pexels.com/photos/9594679/pexels-photo-9594679.jpeg?auto=compress&cs=tinysrgb&w=600',
            name: '潮流服装',
            price: '99.00'
          },
          {
            img: 'https://images.pexels.com/photos/9594679/pexels-photo-9594679.jpeg?auto=compress&cs=tinysrgb&w=600',
            name: '潮流服装',
            price: '99.00'
          },
        ]
      }
    },
    onLoad() {

    },
    methods: {
      search() {
        uni.showToast({
          title: '搜索'
        })
      },
      showCity() {
        uni.showToast({
          title: '选择城市'
        })
      },
      scan() {
        uni.showToast({
          title: '扫码'
        })
      },
      confirm() {
        uni.showToast({
          title: '搜索'
        })
      }
    }
  }
</script>

<style scoped lang="scss">
  .content {
    height: 100%;
    background-color: #f5f5f5;
  }


  swiper {
    height: 300rpx;
  }

  swiper swiper-item {
    height: 100%;
  }

  swiper-item image {
    width: 100%;
    height: 100%;
  }

  .scrollview-box {
    white-space: nowrap;
    width: 100%;
    padding: 20rpx 20rpx 0rpx 20rpx;
  }

  .item {
    width: 300rpx;
    height: 230rpx;
    margin-right: 20rpx;
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    background-color: #ffffff;
    border-radius: 10rpx;
    overflow: hidden;
  }

  .scrollview-box .item image {
    width: 300rpx;
    height: 200rpx;
  }

  .scrollview-box .item .tit {
    font-size: 28rpx;
    width: 100%;
    margin: 10rpx 0;
    line-height: 50rpx;
    display: flex;
    justify-content: space-around;
  }

  .lists-two {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    margin-top: 35rpx;
  }

  .lists-two .item {
    width: 45%;
    margin-bottom: 30rpx;
  }

  .lists-two .item image {
    width: 100%;
    margin-bottom: 10rpx;
  }

  .lists-two .item .title {
    font-size: 28rpx;
  }

  .box {
    margin-top: 10px;
    padding: 30rpx 50rpx;
    background-color: #ffffff;
  }

  .cateBox {
    padding: 30rpx 10px 20rpx;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #ffffff;
  }

  .c-item {
    width: 24%;
    height: 100%;
    text-align: center;
  }

  .c-item image {
    width: 100rpx;
    height: 100rpx;
    border-radius: 10rpx;
  }

  .c-item .tit {
    font-size: 28rpx;
    margin-top: 10rpx;
  }

  .title {
    font-size: 34rpx;
    font-weight: 700;
  }

  .box {}

  .h-item {
    height: 140rpx;
    margin-top: 35rpx;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    box-shadow: #f5f5f5 2px 6rpx;
    border-radius: 10rpx;
  }

  .h-item .left image {
    width: 100rpx;
    height: 100rpx;
    border-radius: 10rpx;
    margin-right: 30rpx;
  }

  .h-item .info {
    width: 60%;
  }

  .h-item .info .tit {
    font-size: 30rpx;
    font-weight: 700;
  }

  .h-item .info .auther {
    font-size: 26rpx;
    margin-top: 10rpx;
    color: #999;
  }

  .icons {
    text-align: end;
    width: 10%;
    font-size: 28rpx;
    color: #999;
  }


  .fx {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }


  $nav-height: 30px;

  .box-bg {
    background-color: #F5F5F5;
    padding: 5px 0;
  }

  .city {
    /* #ifndef APP-PLUS-NVUE */
    display: flex;
    /* #endif */
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    // width: 160rpx;
    margin-left: 4px;
  }

  .input-view {
    /* #ifndef APP-PLUS-NVUE */
    display: flex;
    /* #endif */
    flex-direction: row;
    // width: 500rpx;
    flex: 1;
    background-color: #f8f8f8;
    height: $nav-height;
    border-radius: 15px;
    padding: 0 15px;
    flex-wrap: nowrap;
    margin: 7px 0;
    line-height: $nav-height;
  }

  .input-uni-icon {
    line-height: $nav-height;
  }

  .nav-bar-input {
    height: $nav-height;
    line-height: $nav-height;
    /* #ifdef APP-PLUS-NVUE */
    width: 370rpx;
    /* #endif */
    padding: 0 5px;
    font-size: 12px;
    background-color: #f8f8f8;
  }
</style>

