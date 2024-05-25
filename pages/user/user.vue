<template>
  <view class="content">
    <view class="topBox">
      <uni-icons type="gear" size="32" class="setIcon" color="#fff" @click="setFun"></uni-icons>
      <image src="https://img0.baidu.com/it/u=464193705,1968194224&fm=253&fmt=auto&app=120&f=JPEG?w=801&h=500" mode="aspectFill"></image>
      <view class="userName">
        <view class="name">
          着逝者为铠
        </view>
        <view class="desc">
          以绝望挥剑,着逝者为铠
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
    box-sizing: border-box;
    position: relative;
    height: 100vh;
    background-color: #00aa7f;
  }

  .topBox {
    height: 350rpx;
    padding: 50rpx;
    box-sizing: border-box;
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }

  .topBox image {
    width: 130rpx;
    height: 130rpx;
    border-radius: 50%;
    border: 3rpx solid #fff;
    margin-right: 30rpx;
  }

  .topBox .name {
    font-size: 42rpx;
    color: #fff;
    font-weight: 700;
    margin-bottom: 23rpx;
  }

  .topBox .desc {
    font-size: 28rpx;
    color: #ececec;
    margin-bottom: 10rpx;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-align: center;
  }

  .listBox {
    height: calc(100% - 330rpx);
    background-color: #ffffff;
    border-top-left-radius: 30rpx;
    border-top-right-radius: 30rpx;
    margin-top: -20rpx;
    padding: 30rpx 20rpx;
  }
  
  .setIcon {
    position: absolute;
    top: 50rpx;
    right: 50rpx;
  }
</style>