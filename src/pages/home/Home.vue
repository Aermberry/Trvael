<template>
  <div>
  <home-header :city='city'></home-header>
  <home-swiper :list='swiperList'></home-swiper>
  <home-icons></home-icons>
  <home-recommend></home-recommend>
  <home-weekend></home-weekend>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    /* 这里写成大写，Vue将自动进行关联，组件转换为小写 */
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      swiperList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.jsion').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      console.log(res)
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        console.log(this.swiperList)
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
