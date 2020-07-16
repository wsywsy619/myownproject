<template>
  <div class="head">
    <div class="head1">
    <div class="shou">首页</div>
    <div class="wode">我的音乐</div>
    <div class="icon"><span class="iconfont">&#xe61d;</span></div>
   </div>
  </div>
</template>

<script>
export default {
  name: 'headtop'
}
</script>
<style lang="stylus" scoped>
.head
  position fixed 
  left 0
  right 0
  height 40px
  z-index 100
  background lightblue 
  border-bottom solid 5px lightblue
  .head1
    display flex
    justify-content space-between
    color #fff
    .shou
      width 20%
      text-align center
      line-height 40px
      font-size 20px
      position relative
      &:after/*设置长方形*/
        content: ''
        width 18px
        height 4px
        overflow hidden
        position absolute
        background #fff
        top 85%
        left 50%
        border-radius 9px
        margin-left -9px/*设置长方形居中显示*/
    .wode
      font-size 18px
      text-align left
      line-height 40px
      width 70%
    .icon
      width 10%
      text-align center
      line-height 40px

</style>
