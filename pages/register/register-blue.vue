<template>
  <view class="content">
    <view class="topBox">
      <view class="tit">
        新用户注册
      </view>
      <view class="desc">
        请使用手机号码或邮箱注册账号
      </view>
    </view>

    <view class="bottomBox">
      <view class="item">
        <view class="label">
          账号
        </view>
        <input type="text" value="" placeholder="请输入您的手机号码" />
      </view>
      <view class="item">
        <view class="label">
          密码
        </view>
        <input type="text" value="" placeholder="请输入您的密码" />
      </view>
      <view class="item">
        <view class="label">
          验证码
        </view>
        <view class="yzmBox">
          <input type="text" value="" placeholder="请输入验证码" />
          <view class="yzm" @click="send">
            发送验证码
          </view>
        </view>
      </view>
      <button type="default" @tap="submit">注册</button>
    </view>
    <view class="agree">
      注册代表您同意 xxxxx某某协议
    </view>
  </view>
</template>

<script>
  export default {
    data() {
      return {

      }
    },
    methods: {
      send() {
        uni.showToast({
          title: "发送验证码"
        })
      },
      submit() {
        uni.showToast({
          title: "点击注册",
          icon: "none"
        })
      }
    }
  }
</script>

<style scoped>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .content {
    min-height: 100vh;
  }

  .topBox {
    position: relative;
    height: 400rpx;
    background-color: #00aaff;
  }

  .tit {
    width: 90%;
    font-size: 60rpx;
    color: #ffffff;
    position: absolute;
    bottom: 40%;
    left: 50%;
    transform: translateX(-50%);
    font-weight: 600;
  }

  .desc {
    width: 90%;
    font-size: 30rpx;
    color: #f8f8f8;
    position: absolute;
    bottom: 25%;
    left: 50%;
    transform: translateX(-50%);
  }

  .bottomBox {
    margin-top: 20rpx;
    min-height: 500rpx;
    padding: 50rpx;
  }

  .item {
    margin-bottom: 60rpx;
    border-bottom: 1px solid #ccc;
  }

  .item .label {
    font-size: 32rpx;
    color: #00aaff;
    font-weight: 600;
    margin-bottom: 20rpx;
  }

  .item input {
    height: 70rpx;
    padding-bottom: 20rpx;
    font-size: 32rpx;
    color: #333;
  }

  .uni-input-placeholder {
    color: #bebebe;
  }

  .yzmBox {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .yzm {
    color: #ffffff;
    font-size: 28rpx;
    padding: 5rpx 8rpx;
    background-color: #00aaff;
  }

  button {
    line-height: 85rpx;
    text-align: center;
    background: rgb(0, 170, 255);
    color: #fff;
    margin-top: 100rpx;
  }

  .agree {
    position: fixed;
    bottom: 60rpx;
    left: 0;
    text-align: center;
    width: 100%;
    color: #919191;
    font-size: 30rpx;
  }
</style>