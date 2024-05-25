<template>
  <view class="container">
    <view class="searchBox">
      <uni-section title=''>
        <uni-search-bar placeholder="自定义背景色" bgColor="#ffffff" @confirm="search" />
      </uni-section>
    </view>
    <!--左侧栏-->
    <scroll-view scroll-y="true" class="nav_left">
      <block v-for="(item,index) in leftList" :key="item.id">
        <view class="nav_left_items" :class="index == isActive?'active':''" @click="clickFun(item.id,index)">
          {{item.tit}}
        </view>
      </block>
    </scroll-view>
    <!--右侧栏-->
    <scroll-view scroll-y="true" class="nav_right">
      <view>
        <block v-for="(item,index) in rights" :key="item.id">
          <view class="nav_right_items">
            <label>
              <image :src="item.img"></image>
              <text>{{item.tit}}</text>
            </label>
          </view>
        </block>
      </view>
      <!--如果无数据，则显示数据-->
      <view class="nodata_text" v-if="rights.length == 0">该分类暂无数据</view>
    </scroll-view>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        leftList: [{
          id: 1,
          tit: '电视',
        }, {
          id: 2,
          tit: '电脑',
        }, {
          id: 3,
          tit: '手机',
        }, {
          id: 4,
          tit: '家具',
        }, {
          id: 5,
          tit: '冰箱',
        }],
        rights: [],
        rightList: [
          [{
              id: 1,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
            {
              id: 2,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
            {
              id: 3,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
            {
              id: 4,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
            {
              id: 5,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
            {
              id: 6,
              tit: '海尔电视',
              img: '../../static/logo.png'
            },
          ],
          [{
              id: 1,
              tit: '联想电脑',
              img: '../../static/logo.png'
            },
            {
              id: 2,
              tit: '联想电脑',
              img: '../../static/logo.png'
            },
            {
              id: 3,
              tit: '联想电脑',
              img: '../../static/logo.png'
            },
            {
              id: 4,
              tit: '联想电脑',
              img: '../../static/logo.png'
            },
            {
              id: 5,
              tit: '联想电脑',
              img: '../../static/logo.png'
            }
          ],
          [{
              id: 1,
              tit: '小米手机',
              img: '../../static/logo.png'
            },
            {
              id: 2,
              tit: '小米手机',
              img: '../../static/logo.png'
            },
            {
              id: 3,
              tit: '小米手机',
              img: '../../static/logo.png'
            },
            {
              id: 4,
              tit: '小米手机',
              img: '../../static/logo.png'
            },
            {
              id: 5,
              tit: '小米手机',
              img: '../../static/logo.png'
            }
          ],
          [{
              id: 1,
              tit: '家具',
              img: '../../static/logo.png'
            },
            {
              id: 2,
              tit: '家具',
              img: '../../static/logo.png'
            },
            {
              id: 3,
              tit: '家具',
              img: '../../static/logo.png'
            },
            {
              id: 4,
              tit: '家具',
              img: '../../static/logo.png'
            }
          ],
          [{
              id: 1,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },
            {
              id: 2,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },
            {
              id: 3,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },
            {
              id: 4,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },
            {
              id: 5,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },
            {
              id: 6,
              tit: 'xxx冰箱',
              img: '../../static/logo.png'
            },

          ]
        ],
        isActive: 0,
      }
    },
    onShow() {
      this.rights = this.rightList[0]
    },
    methods: {
      clickFun(id, index) {
        console.log(id, index);
        this.rights = this.rightList[id - 1]
        this.isActive = index
      }
    }
  }
</script>

<style scoped>
  page {
    background: #f5f5f5;
  }

  .container {
    position: relative;
    width: 100%;
    height: calc(100vh - 149.8rpx);
    background-color: #fff;
    color: #939393;
  }

  .searchBox {
    width: 100%;
    padding-bottom: 10rpx;
  }

  /*左侧*/
  .nav_left {
    display: inline-block;
    width: 25%;
    height: calc(100vh - 200rpx);
    background: #f5f5f5;
    text-align: center;
  }

  /*左侧项*/
  .nav_left .nav_left_items {
    line-height: 70rpx;
    padding: 12rpx 0;
    font-size: 14px;
  }

  .nav_left .nav_left_items.active {
    background: #00aa7f;
    color: #fff;
  }

  /*右侧*/
  .nav_right {
    position: absolute;
    top: 160rpx;
    right: 0;
    flex: 1;
    width: 75%;
    height: calc(100vh - 190rpx);
    padding: 0;
    box-sizing: border-box;
    background: #fff;
  }

  .nav_right .nav_right_items {
    float: left;
    width: 33.33%;
    height: 120px;
    text-align: center;
  }

  .nav_right .nav_right_items image {
    width: 60px;
    height: 60px;
    margin-top: 15px;
  }

  .nav_right .nav_right_items text {
    display: block;
    margin-top: 15rpx;
    font-size: 26rpx;
    color: black;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }

  .nodata_text {
    color: black;
    font-size: 14px;
    text-align: center;
  }

  /deep/.uni-searchbar__box {
    border: 1px solid #00aa7f !important;
    border-radius: 33rpx !important;
  }
</style>