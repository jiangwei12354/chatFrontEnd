<template>
  <view class="content">
    <view class="list">
      <view class="list-left">
        <uni-badge absolute="rightTop" text="2">
          <img src="" alt="" />
        </uni-badge>
      </view>
      <view class="list-center">
        <view class="list-name">hha</view>
        <view class="list-content">asdfoji</view>
      </view>
      <view class="list-right">
        <view class="list-time">20:01</view>
        <view class="list-icon"></view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  onLoad: function () {},
};
</script>

<style lang="scss" scoped>
.content {
}
/deep/.uni-badge--x {
  width: 100%;
  height: 100%;
}
.list {
  display: flex;
  padding: 20rpx 30rpx;
  align-items: center;
  background: #fff;
  .list-left {
    width: 100rpx;
    height: 100rpx;
    img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
    }
  }
  .list-center {
    flex: 1;
    margin-left: 20rpx;
    display: inline-flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    .list-name {
      font-weight: 500;
      font-size: 30rpx;
    }
    .list-content {
      color: #8f8c8c;
    }
  }
  .list-right {
  }
}
</style>
