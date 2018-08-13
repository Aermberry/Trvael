<template>
  <div>
  <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img">
          <img class="item-img" :src="item.imgurl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title" v-text="item.title"></p>
          <p class="item-desc" v-text="item.desc"></p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/sight/source/1711/15/1cdd5ee885686b.jpg_r_640x214_46768064.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/sight/source/1511/8f/bf3a40e4afcf29.jpg_r_640x214_90225212.jpg',
        title: '棕榈谷水城',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0003',
        imgurl: 'http://img1.qunarzz.com/sight/source/1505/b3/671f666cc7845a.jpg_r_640x214_f977f30c.jpg',
        title: '东莞香市动物园',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0004',
        imgurl: 'http://img1.qunarzz.com/sight/source/1505/ae/15c0516f565a02.jpg_r_640x214_b8176bc2.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0005',
        imgurl: 'http://img1.qunarzz.com/sight/source/1606/53/c5ebb7bf59681b.jpg_r_640x214_8cf5e397.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0006',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0007',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0008',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0009',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }]
    }
  }

}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
      .title
        margin-top .2rem
        line-height .8rem
        background #eeeeee
        text-indent .2rem//缩进行首
      .item-img-wrapper
        overflow
        height 0
        padding-bottom 33.9%
      .item-img
        width 100%
        // width 1.7rem
        // height 1.7rem
        // padding .1rem
      .item-info
        padding .1rem
        // min-width 0
        .item-title
          line-height .54rem
          font-size .32rem
          ellipsis()
        .item-desc
          line-height .4rem
          color #cccccc
          ellipsis()
</style>
