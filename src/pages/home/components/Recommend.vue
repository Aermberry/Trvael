<template>
  <div>
  <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgurl" alt="">
        <div class="item-info">
          <p class="item-title" v-text="item.title"></p>
          <p class="item-desc" v-text="item.desc"></p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1607/6c/6ce376cd5775ce6fb4.img.jpg_200x200_7ed7ce79.jpg',
        title: '棕榈谷水城',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0003',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1603/1d/1d756648039bf30f90.water.jpg_200x200_64da9a70.jpg',
        title: '东莞香市动物园',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0004',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '隐贤山庄',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      },
      {
        id: '0005',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
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
      .item
        display flex
        // background red
        overflow hidden
        height 1.9rem
        .item-img
          width 1.7rem
          height 1.7rem
          padding .1rem
        .item-info
          flex 1
          padding .1rem
          min-width 0
          .item-title
            line-height .54rem
            font-size .32rem
            ellipsis()
          .item-desc
            line-height .4rem
            color #cccccc
            ellipsis()
          .item-button
            line-height .44rem
            margin-top .16rem
            background #ff9300
            padding 0 .2rem
            border-radius .6rem
            color #ffffff
</style>
