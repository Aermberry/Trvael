<template>
<div class="wrapper">
<swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperlist" :key="item.id">
      <img class="swiper-img" :src="item.imgurl" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      },
      swiperlist: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1806/de/df09fa61aed2d502.jpg_750x200_67472739.jpg'
      },
      {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1805/e8/14b75b1c81fbe702.jpg_750x200_e6d4f1f1.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>>  .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 26.5%
    /* 如果值是一个百分比，那这个百分比时相对于其父元素的宽度而言的 */
    background-color #eeeeee
    .swiper-img
      width 100%
</style>
