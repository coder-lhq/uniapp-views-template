<template>
  <view class="content">

    <view class="yhq1" :class="item.isUse?'use':''" v-for="(item,index) in yhqList1" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
          </view>
        </view>
      </view>
    </view>

    <view class="yhq2" :class="item.isUse?'use':''" v-for="(item,index) in yhqList2" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
          </view>
        </view>
      </view>
    </view>

    <view class="yhq3" :class="item.isUse?'use':''" v-for="(item,index) in yhqList3" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
          </view>
        </view>
      </view>
    </view>

    <view class="yhq4" :class="item.isUse?'use':''" v-for="(item,index) in yhqList4" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
          </view>
        </view>
      </view>
    </view>

    <view class="yhq5" :class="item.isUse?'use':''" v-for="(item,index) in yhqList5" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
          </view>
        </view>
      </view>
    </view>

    <view class="yhq6" :class="item.isUse?'use':''" v-for="(item,index) in yhqList6" @click="click(item)">
      <view class="left">
        ￥{{item.price}}
      </view>
      <view class="right">
        <view class="tit">
          {{item.title}}
        </view>
        <view class="desc">
          <view class="p">
            {{item.time}}
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
        isUse: false, // 是否已使用
        yhqList1: [{
            isUse: false,
            title: '某某商品优惠券11',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券12',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
        yhqList2: [{
            isUse: false,
            title: '某某商品优惠券21',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券22',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
        yhqList3: [{
            isUse: false,
            title: '某某商品优惠券31',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券32',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
        yhqList4: [{
            isUse: false,
            title: '某某商品优惠券41',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券42',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
        yhqList5: [{
            isUse: false,
            title: '某某商品优惠券51',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券52',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
        yhqList6: [{
            isUse: false,
            title: '某某商品优惠券61',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
          {
            isUse: false,
            title: '某某商品优惠券62',
            price: '100',
            time: '有效期至: 2025年10月1日'
          },
        ],
      }
    },
    methods: {
      click(item) {
        console.log(item);
        uni.showToast({
          title: "使用优惠券",
          icon: "none"
        })
        item.isUse = true
      }
    }
  }
</script>

<style>
  .content {
    padding: 20rpx;
  }

  .yhq1 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background: linear-gradient(to right, #aa55ff, #ff007f);
    -webkit-mask: radial-gradient(circle at 20px 20px, #0000 20px, blue 0);
    -webkit-mask-position: -20px -20px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }

  .use {
    filter: grayscale(1);
  }

  .left {
    width: 20%;
    font-size: 50rpx;
    font-weight: 700;
    color: #fff;
  }

  .right .tit {
    font-size: 33rpx;
    color: #fff;
    font-weight: 600;
  }

  .right .desc .p {
    font-size: 28rpx;
    color: #d8d8d8;
    margin-top: 10rpx;
  }

  .yhq2 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background-image: linear-gradient(to top, #ff0844 0%, #ffb199 100%);
    -webkit-mask: radial-gradient(circle at 20px, #0000 16px, blue 0);
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }

  .yhq3 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background: linear-gradient(45deg, #aa55ff, #00aaff);
    -webkit-mask: radial-gradient(circle at 0, #0000 20px, blue 0), radial-gradient(circle at right, #0000 20px, blue 0);
    -webkit-mask-size: 51%;
    -webkit-mask-position: 0, 100%;
    -webkit-mask-repeat: no-repeat;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }

  .yhq3 .left {
    width: 35%;
    height: 100%;
    display: flex;
    align-items: center;
    border-right: 1px dashed #fff;
  }

  .yhq3 .right {
    width: 55%;
    text-align: center;
  }


  .yhq4 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background-image: linear-gradient(to right, #fa709a 0%, #ff00ff 100%);
    -webkit-mask: radial-gradient(circle at 10px, #0000 10px, blue 0);
    -webkit-mask-position: -10px;
    -webkit-mask-size: 100% 30px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }

  .yhq5 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background-image: linear-gradient(120deg, #00aa7f 0%, #8fd3f4 100%);
    -webkit-mask: radial-gradient(circle at 20px 20px, #0000 20px, blue 0);
    -webkit-mask-position: -20px -20px;
    -webkit-mask-size: 50%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }

  .yhq5 .left {
    width: 35%;
    height: 100%;
    display: flex;
    align-items: center;
    border-right: 1px dashed #fff;
  }

  .yhq5 .right {
    width: 55%;
    text-align: center;
  }

  .yhq6 {
    width: 100%;
    height: 100px;
    margin-top: 15px;
    background: linear-gradient(45deg, #ff0000, #ff11ff);
    -webkit-mask: radial-gradient(circle at left center, transparent 20px, blue 20px);
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20rpx 30rpx 20rpx 50rpx;
    box-sizing: border-box;
  }
</style>