<template>
  <view class="content">
    <view class="topBox">
      <view class="setbox">
        <view class="set-left">
          <uni-icons type="calendar" size="30" color="#fff"></uni-icons>
          <view class="txt">签到</view>
        </view>
        <view class="set-right">
          <uni-icons type="gear" size="30" color="#fff" @click="setFun"></uni-icons>
          <uni-icons type="chat" size="30" color="#fff"></uni-icons>
        </view>
      </view>

      <view class="users">
        <view class="u-top">
          <image
            src="https://img2.baidu.com/it/u=2953585264,744730101&fm=253&fmt=auto&app=138&f=JPEG?w=360&h=360"
            mode=""></image>
          <view class="tit">
            登录 / 注册
          </view>
        </view>
        <view class="u-bottom">
          <view class="u-item">
            <view class="num">12</view>
            <view class="u-tit">浏览</view>
          </view>
          <view class="u-item">
            <view class="num">12</view>
            <view class="u-tit">浏览</view>
          </view>
          <view class="u-item">
            <view class="num">12</view>
            <view class="u-tit">浏览</view>
          </view>
        </view>
      </view>
    </view>

    <view class="bottomBox">
      <view class="order-list">
        <view class="o-item">
          <image src="../../static/daifuk.png" mode=""></image>
          <view class="tit">待付款</view>
        </view>
        <view class="o-item">
          <image src="../../static/daifa.png" mode=""></image>
          <view class="tit">待发货</view>
        </view>
        <view class="o-item">
          <image src="../../static/yifa.png" mode=""></image>
          <view class="tit">已发货</view>
        </view>
        <view class="o-item">
          <image src="../../static/wancheng.png" mode=""></image>
          <view class="tit">已完成</view>
        </view>
      </view>
    </view>

    <view class="listBox">
      <view class="lists">
        <uni-list>
          <uni-list-item :show-extra-icon="true" :extra-icon="extraIcon1" showArrow title="个人信息" clickable
            @click="clickList" rightText="右侧文字" />
          <uni-list-item :show-extra-icon="true" :extra-icon="extraIcon2" showArrow title="我的购物车" clickable
            @click="clickList" rightText="右侧文字" />
          <uni-list-item :show-extra-icon="true" :extra-icon="extraIcon3" showArrow title="用户反馈" clickable
            @click="clickList" />
          <uni-list-item :show-extra-icon="true" :extra-icon="extraIcon4" showArrow title="我的邮件" clickable
            @click="clickList" />
          <uni-list-item :show-extra-icon="true" :extra-icon="extraIcon5" showArrow title="分享有礼" clickable
            @click="clickList" />
        </uni-list>
      </view>
    </view>

  </view>
</template>

<script>
  export default {
    data() {
      return {
        extraIcon1: {
          color: '#666666',
          size: '22',
          type: 'auth'
        },
        extraIcon2: {
          color: '#666666',
          size: '22',
          type: 'cart'
        },
        extraIcon3: {
          color: '#666666',
          size: '22',
          type: 'chatboxes'
        },
        extraIcon4: {
          color: '#666666',
          size: '22',
          type: 'email'
        },
        extraIcon5: {
          color: '#666666',
          size: '22',
          type: 'gift'
        },

      }
    },
    methods: {
      setFun() {
        uni.showToast({
          title: "点击设置",
          icon: "none"
        })
      },
      clickList() {
        uni.showToast({
          title: "点击列表",
          icon: "none"
        })
      }
    }
  }
</script>

<style scoped>
  .content {
    background-color: #f5f5f5;
    height: 100vh;
  }

  /* 弧形背景 */
  .topBox {
    width: 100%;
    position: relative;
    z-index: 1;
    overflow: hidden;
    padding: 60rpx 20rpx 20rpx;
    box-sizing: border-box;
  }

  .topBox::after {
    content: "";
    width: 140%;
    height: 200px;
    position: absolute;
    left: -20%;
    top: 0;
    z-index: -1;
    border-radius: 0 0 50% 50%;
    background: #00aaff;
  }

  /* 弧形背景 */
  
  .setbox {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .set-left {
    width: 18%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .txt {
    color: #fff;
    font-size: 30rpx;
  }

  .set-right .uni-icons {
    margin-right: 10rpx;
  }

  .users {
    margin-top: 20rpx;
    padding: 30rpx;
    box-sizing: border-box;
    height: 280rpx;
    background-color: #fff;
    box-shadow: 1px 10rpx 20rpx #ececec;
    border-radius: 12rpx;
  }

  .u-top {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin-bottom: 30rpx;
  }

  .users .u-top image {
    width: 100rpx;
    height: 100rpx;
    border-radius: 50%;
    margin-right: 20rpx;
  }

  .u-top .tit {
    font-size: 30rpx;
    font-weight: 700;
    color: #333;
  }

  .u-bottom {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .u-item {
    text-align: center;
  }

  .u-item .u-tit {
    color: #757575;
    font-size: 26rpx;
    margin-top: 10rpx;
  }

  .u-item .num {
    color: #000000;
    font-size: 33rpx;
    font-weight: 700;
  }

  .bottomBox {
    padding: 20rpx;
    box-sizing: border-box;
  }

  .order-list {
    height: 200rpx;
    margin: -15rpx auto 0;
    padding: 30rpx;
    box-sizing: border-box;
    background-color: #fff;
    border-radius: 12rpx;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .o-item {
    width: 25%;
    text-align: center;
  }

  .o-item image {
    width: 65rpx;
    height: 55rpx;
  }

  .o-item .tit {
    font-size: 28rpx;
    margin-top: 10rpx;
  }

  .listBox {
    height: 200rpx;
    margin: -10rpx auto 0;
    padding: 20rpx;
    box-sizing: border-box;
    border-radius: 12rpx;
  }
</style>