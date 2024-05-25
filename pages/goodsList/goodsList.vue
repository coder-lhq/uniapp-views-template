<template>
  <view class="content">
    <div class="tops">
      <div class="t-item">综合</div>
      <div class="t-item">销量</div>
      <div class="t-item choose" @click="clickPrice">
        <span>价格</span>
        <span v-if="isPrice">
          <svg t="1712993436208" class="icon" viewBox="0 0 1024 1024" version="1.1"
            xmlns="http://www.w3.org/2000/svg" p-id="6150" width="15" height="15">
            <path d="M512 0l307.2 409.6H204.8z" fill="#EB6A0D" p-id="6151"></path>
            <path d="M512 1024l307.2-409.6H204.8z" fill="#EBEBEB" p-id="6152"></path>
          </svg>
        </span>
        <span v-else>
          <svg t="1712993501022" class="icon" viewBox="0 0 1024 1024" version="1.1"
            xmlns="http://www.w3.org/2000/svg" p-id="6301" width="15" height="15">
            <path d="M512 0l307.2 409.6H204.8z" fill="#EBEBEB" p-id="6302"></path>
            <path d="M512 1024l307.2-409.6H204.8z" fill="#EB6A0D" p-id="6303"></path>
          </svg>
        </span>
      </div>
      <div class="t-item">筛选</div>
    </div>

    <div class="lists">
      <div class="l-item" v-for="(item,index) in 20" :key="index">
        <image
          src="https://images.pexels.com/photos/5272964/pexels-photo-5272964.jpeg?auto=compress&cs=tinysrgb&w=600"
          mode="aspectFill"></image>
        <view class="desc">
          <view class="tit">
            商品名称商品名称
          </view>
          <view class="infos">
            <view class="price">
              <span class="buyPrice">￥120.00</span>
              <span class="hua">￥120.00</span>
            </view>
            <view class="btn">
              去购买
            </view>
          </view>
        </view>
      </div>
    </div>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        isPrice: false,
      }
    },
    methods: {
      clickPrice() {
        this.isPrice = !this.isPrice
      },
    }
  }
</script>

<style scoped>
  .content {
    min-height: calc(100vh - 88rpx);
    padding: 0rpx 35rpx 20rpx;
    box-sizing: border-box;
    background-color: #f5f5f5;
  }

  .tops {
    position: fixed;
    top: 80rpx;
    left: 0;
    width: 100%;
    z-index: 99;
    padding: 0rpx 35rpx;
    box-sizing: border-box;
    display: flex;
    justify-content: space-around;
    align-items: center;
    line-height: 70rpx;
    background-color: #fff;
    box-shadow: 2rpx 2rpx 10rpx #eee;
  }

  .tops .t-item {
    font-size: 30rpx;
    color: #333;
  }

  .t-item:hover {
    color: #ff5500;
  }

  .choose {
    display: flex;
    align-items: center;
  }

  .choose span {
    margin-right: 5rpx;
  }

  .lists {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding-top: 60rpx;
  }

  .l-item {
    width: 48%;
    box-shadow: 2rpx 2rpx 10rpx #bdbdbd;
    background-color: #fff;
    margin-top: 30rpx;
  }

  .l-item image {
    width: 100%;
    height: 200rpx;
    margin-bottom: 2rpx;
  }

  .l-item .desc .tit {
    font-size: 28rpx;
    color: #333;
    font-weight: 700;
    margin-bottom: 5rpx;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }

  .l-item .desc {
    padding: 10rpx;
    box-sizing: border-box;
  }

  .l-item .desc .infos {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .price span {
    margin-right: 15rpx;
    font-size: 28rpx;
  }

  .buyPrice {
    color: #ff5500;
    font-weight: 700;
  }

  .hua {
    text-decoration: line-through;
    color: #999;
    font-size: 24rpx !important;
  }

  .btn {
    font-size: 28rpx;
    border: 1px solid #ff5500;
    color: #ff5500;
    text-align: center;
    width: 100%;
    line-height: 45rpx;
    margin-top: 10rpx;
    border-radius: 8rpx;
  }

  .btn:hover {
    background-color: #ff5500;
    color: #fff;
  }
</style>