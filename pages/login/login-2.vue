<template>
  <view class="content">
    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMax slice">
      <defs>
        <linearGradient id="bg">
          <stop offset="0%" style="stop-color:rgba(130, 158, 249, 0.06)"></stop>
          <stop offset="50%" style="stop-color:rgba(76, 190, 255, 0.6)"></stop>
          <stop offset="100%" style="stop-color:rgba(115, 209, 72, 0.2)"></stop>
        </linearGradient>
        <path id="wave" fill="url(#bg)"
          d="M-363.852,502.589c0,0,236.988-41.997,505.475,0
          s371.981,38.998,575.971,0s293.985-39.278,505.474,5.859s493.475,48.368,716.963-4.995v560.106H-363.852V502.589z" />
      </defs>
      <g>
        <use xlink:href='#wave' opacity=".3">
          <animateTransform attributeName="transform" attributeType="XML" type="translate" dur="10s"
            calcMode="spline" values="270 230; -334 180; 270 230" keyTimes="0; .5; 1"
            keySplines="0.42, 0, 0.58, 1.0;0.42, 0, 0.58, 1.0" repeatCount="indefinite" />
        </use>
        <use xlink:href='#wave' opacity=".6">
          <animateTransform attributeName="transform" attributeType="XML" type="translate" dur="8s"
            calcMode="spline" values="-270 230;243 220;-270 230" keyTimes="0; .6; 1"
            keySplines="0.42, 0, 0.58, 1.0;0.42, 0, 0.58, 1.0" repeatCount="indefinite" />
        </use>
        <use xlink:href='#wave' opacty=".9">
          <animateTransform attributeName="transform" attributeType="XML" type="translate" dur="6s"
            calcMode="spline" values="0 230;-140 200;0 230" keyTimes="0; .4; 1"
            keySplines="0.42, 0, 0.58, 1.0;0.42, 0, 0.58, 1.0" repeatCount="indefinite" />
        </use>
      </g>
    </svg>
    
    <view class="loginBox">
      <h3 style="text-align: center;margin-bottom:120rpx;">欢迎登录</h3>
      <view class="inputBox">
        <view class="ipt">
          <uni-icons type="contact" size="24" color="rgb(66,157,250)"></uni-icons>
          <input type="text" value="" placeholder="请输入账号"/>
        </view>
        <view class="ipt">
          <uni-icons type="eye" size="24" color="rgb(66,157,250)"></uni-icons>
          <input type="passsword" value="" placeholder="请输入密码"/>
        </view>
        <view class="ipt">
          <uni-icons type="checkmarkempty" size="24" color="rgb(66,157,250)"></uni-icons>
          <input type="text" value="" placeholder="请输入验证码"/>
          <view class="yzm">
            验证码
          </view>
        </view>
        <button>登录</button>
        <view class="forgetPwd">
          <span>忘记密码</span>
          <span>没有账号，去注册</span>
        </view>
      </view>
      <view class="tipbox">
        <view class="txt">
          —— 其他账号登录 ——
        </view>
        <view class="otherUser">
          <uni-icons type="qq" size="40" color="rgb(66,157,250)"></uni-icons>
          <uni-icons type="weixin" size="40" color="rgb(2,187,17)"></uni-icons>
        </view>
      </view>
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

    }
  }
</script>

<style scoped>
  svg {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height:40%;
    box-sizing: border-box;
    display: block;
    background-color: #ffffff;
  }
  
  .loginBox{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-60%);
    width: 90%;
    border-radius: 20rpx;
    padding: 60rpx;
    box-sizing: border-box;
  }
  h3{
    color:rgb(66,157,250);
    font-size: 40rpx;
    letter-spacing: 10rpx;
    margin-bottom: 40rpx;
  }
  .inputBox{
    
  }
  .ipt{
    height: 86rpx;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin-bottom: 40rpx;
    background-color: #f5f5f5;
    border-radius: 10rpx;
    padding-left: 10rpx;
  }
  .ipt input{
    margin-left: 20rpx;
    font-size: 28rpx;
  }
  .ipt input{
    margin-left: 20rpx;
  }
  .forgetPwd{
    margin-top: 30rpx;
    font-size: 26rpx;
    color: #b5b5b5;
    text-align: end;
    padding:0 10rpx;
    display: flex;
    justify-content: space-between;
  }
  button{
    margin-top: 20rpx;
    line-height: 85rpx;
    text-align: center;
    background: rgb(66,157,250);
    border-radius: 40rpx;
    color: #fff;
    margin-top: 40rpx;
  }
  
  .tip{
    text-align: center;
    font-size: 28rpx;
    position: fixed;
    bottom: 50rpx;
    left: 50%;
    transform: translate(-50%,-50%);
    color: #f4f4f4;
  }
  .tipbox {
    text-align: center;
    margin-top: 100rpx;
  }
  
  .otherUser {
    margin-top: 30rpx;
    display: flex;
    justify-content: center;
  }
  
  .txt {
    font-size: 28rpx;
    color: #cbcbcb;
  }
  
  .otherUser .uni-icons {
    margin-left: 20rpx;
  }
  .yzm{
    text-align: end;
    font-size: 24rpx;
    background: linear-gradient(to right,rgb(66,157,250),rgb(0, 170, 127));
    height: 60rpx;
    width: 150rpx;
    line-height: 60rpx;
    text-align: center;
    border-radius: 10rpx;
    color: #fff;
  }
</style>