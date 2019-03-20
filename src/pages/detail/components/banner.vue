<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1812/8d/8dd20c66111af48ea3.img.jpg_600x330_2db60006.jpg" />
      <div class="banner-info">
        <div class="banner-title">杭州千岛湖</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe633;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="close"></common-gallary>
  </div>
</template>

<script>
  import CommonGallary from 'common/gallary/gallary';
  export default {
    name: 'DetailBanner',
    data() {
      return {
        showGallary: false,
        imgs: ['http://img1.qunarzz.com/sight/p0/201406/24/9fb4bea11d3cf441cfe7ceffe77dec6c.jpg_r_800x800_355296d6.jpg']
      };
    },
    methods: {
      handleBannerClick() {
        this.showGallary = true;
      },
      close() {
        this.showGallary = false;
      }
    },
    components: {
      CommonGallary
    }
  };
</script>

<style lang="stylus" scoped>
  .banner
    position: relative;
    overflow: hidden;
    height: 0;
    padding-bottom: 55%;
    .banner-img
      width: 100%;
    .banner-info
      display: flex;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      line-height: .6rem;
      color: #FFFFFF;
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));
      .banner-title
        flex: 1;
        font-size: .32rem;
        padding: 0 .2rem;
      .banner-number
        height: .32rem;
        line-height: .32rem;
        margin-top: .14rem;
        padding: 0 .4rem;
        border-radius: .2rem;
        background: rgba(0, 0, 0, .8);
        font-size: .24rem;
        .banner-icon
          font-size: .24rem;
          padding-right: .1rem;
</style>
