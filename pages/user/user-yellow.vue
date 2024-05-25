<template>
  <view class="content">
    <view class="tops">
      <uni-icons type="gear" size="32" class="setIcon" @click="setFun"></uni-icons>
      <view class="infos">
        <image
          src="https://img1.baidu.com/it/u=1665929857,2089570148&fm=253&fmt=auto&app=120&f=JPEG?w=500&h=889"
          mode="aspectFill"></image>
        <view class="names">
          韩信
        </view>
        <view class="desc">
          纵情山河万里，肆意九州五岳，爱恨痴狂，抵不过沧海一笑
        </view>
        <view class="t-list">
          <view class="t-item">
            <view class="tit">
              收藏
            </view>
            <view class="vals">
              45
            </view>
          </view>
          <view class="t-item">
            <view class="tit">
              点赞
            </view>
            <view class="vals">
              266
            </view>
          </view>
          <view class="t-item">
            <view class="tit">
              分享
            </view>
            <view class="vals">
              103
            </view>
          </view>
        </view>
      </view>

    </view>

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
        }
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
  .tops {
    position: relative;
    height: 580rpx;
    background-color: aquamarine;
    background: url("https://img1.baidu.com/it/u=3643237076,897388802&fm=253&fmt=auto&app=138&f=JPEG?w=800&h=400") no-repeat;
    background-size: 100% 100%;
  }

  .setIcon {
    position: absolute;
    top: 50rpx;
    right: 50rpx;
  }

  .lists {
    padding: 20rpx;
  }

  .tops .infos {
    width: 80%;
    height: 450rpx;
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -25%);
    text-align: center;
  }

  .infos image {
    width: 120rpx;
    height: 120rpx;
    border-radius: 50%;
    border: 4rpx solid #fff;
  }

  .infos .names {
    font-size: 34rpx;
    color: #333;
    font-weight: 700;
    margin: 20rpx 0 10rpx;
  }

  .infos .desc {
    max-width: 62%;
    font-size: 28rpx;
    color: #333;
    margin: 10rpx auto;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-align: center;
  }

  .infos .t-list {
    margin-top: 60rpx;
    display: flex;
    justify-content: space-around;
  }

  .t-item .tit {
    font-size: 32rpx;
    color: #333;
    margin-bottom: 10rpx;
  }

  .t-item .vals {
    font-size: 36rpx;
    color: #333;
    font-weight: 700;
    margin-bottom: 10rpx;
  }

  /deep/.uni-list-item__content-title[data-v-296a3d7e] {
    font-size: 30rpx;
    color: #333;
    overflow: hidden;
    font-weight: 500;
  }

  /deep/.uni-list-item__container {
    padding: 30rpx;
  }
</style>