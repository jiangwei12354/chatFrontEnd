<template>
  <view class="work-container"> </view>
</template>

<script>
export default {
  data() {
    return {
      current: 0,
      swiperDotIndex: 0,
      data: [
        {
          image: "/static/images/banner/banner01.jpg",
        },
        {
          image: "/static/images/banner/banner02.jpg",
        },
        {
          image: "/static/images/banner/banner03.jpg",
        },
      ],
    };
  },
  methods: {
    clickBannerItem(item) {
      console.info(item);
    },
    changeSwiper(e) {
      this.current = e.detail.current;
    },
    changeGrid(e) {
      this.$modal.showToast("模块建设中~");
    },
  },
};
</script>

<style lang="scss">
/* #ifndef APP-NVUE */
page {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  // background-color: #fff;
  min-height: 100%;
  height: auto;
}

view {
  font-size: 14px;
  line-height: inherit;
}

/* #endif */

.text {
  text-align: center;
  font-size: 26rpx;
  margin-top: 10rpx;
}

.grid-item-box {
  flex: 1;
  /* #ifndef APP-NVUE */
  display: flex;
  /* #endif */
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 15px 0;
}

.uni-margin-wrap {
  width: 690rpx;
  width: 100%;
}

.swiper {
  height: 300rpx;
}

.swiper-box {
  height: 150px;
}

.swiper-item {
  /* #ifndef APP-NVUE */
  display: flex;
  /* #endif */
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #fff;
  height: 300rpx;
  line-height: 300rpx;
}

@media screen and (min-width: 500px) {
  .uni-swiper-dot-box {
    width: 400px;
    /* #ifndef APP-NVUE */
    margin: 0 auto;
    /* #endif */
    margin-top: 8px;
  }

  .image {
    width: 100%;
  }
}
</style>
