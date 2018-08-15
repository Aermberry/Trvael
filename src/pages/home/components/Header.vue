<template>
<div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xeacd;</div>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xeac6;</span>
    输入城市/景点/游玩主题</div>
  <div class="header-right">
    {{this.city}}
    <span class="iconfont arrow-icon">&#xeac1;</span>
    </div>
</div>
</template>
<script>
export default {
  name: 'Home',
  props: {
    city: {
      type: String
    }
  }
}
</script>

<style lang="stylus" scoped>
/* @代表src目录 */
/* css引入其他css需要用@important */
/* css中引入其他的css项并使用@符号需要在前面添加 ~ */
@import '~styles/varibles.styl';
  .header
    display flex
    line-height .86rem
    background $bgColor
    color #ffffff
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-left  .2rem
      padding-left .2rem
      background #ffffff
      border-radius .1rem
      color #cccccc
    .header-right
      width 1.24rem
      float right
      text-align center
      .arrow-icon
        font-size .24rem
</style>
