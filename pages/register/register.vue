<template>
  <view class="content">
    <view class="box">
      <view class="tit">
        欢迎注册
      </view>
      <view class="desc">
        请使用手机号码注册账号
      </view>

      <form action="">
        <view class="item">
          <view class="ll">
            +86
          </view>
          <input type="text" value="" placeholder="请输入手机" />
        </view>
        <view class="item">
          <input type="text" value="" placeholder="请输入验证码" />
          <view class="rr" @click="send">
            发送验证码
          </view>
        </view>

        <button type="default" @tap="submit">注册</button>
      </form>
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
    min-height: calc(100vh - 0rpx);
    background: url("https://img1.baidu.com/it/u=1172319054,1238102685&fm=253&fmt=auto&app=138&f=JPEG?w=266&h=400") no-repeat;
    background-size: cover;
  }

  .box {
    position: fixed;
    top: 38%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 90%;
  }

  .tit {
    font-size: 70rpx;
    color: #fff;
    font-weight: 666;
    letter-spacing: 5rpx;
    padding: 10rpx;
  }

  .desc {
    margin-top: 15rpx;
    font-size: 30rpx;
    color: #e5e5e5;
    margin-bottom: 50rpx;
    padding: 10rpx;
  }

  .item {
    margin-bottom: 50rpx;
    border-radius: 50rpx;
    padding: 5rpx 30rpx;
    height: 100rpx;
    background-color: rgba(109, 109, 109, 0.5);
    display: flex;
    align-items: center;
  }

  .ll {
    margin-right: 20rpx;
    color: #fff;
    font-weight: 600;
  }

  input {
    width: 75%;
    color: #fff;
    font-size: 32rpx;
  }

  .rr {
    width: 25%;
    font-size: 28rpx;
    color: #fff;
  }

  .uni-input-placeholder {
    color: #d1d1d1;
  }

  button {
    border-radius: 50rpx;
    background-color: #ffffff;
    color: #000000;
  }

  .agree {
    position: fixed;
    bottom: 230rpx;
    left: 0;
    text-align: center;
    width: 100%;
    color: #b6b6b6;
    font-size: 30rpx;
  }
</style>