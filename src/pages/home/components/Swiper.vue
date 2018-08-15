<template>
<div class="wrapper">
<swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: {
      type: Array
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 30%;
  /* 如果值是一个百分比，那这个百分比时相对于其父元素的宽度而言的 */
  background-color: #eeeeee;

  .swiper-img {
    width: 100%;
  }
}
</style>
