<template>
  <div class="head">
    <div class="left"><div class="content"><div><ul><li><span class="iconfont">&#xe602;</span><span> 魏思远</span></li><li><span class="iconfont">&#xe619;</span><span> 21</span></li><li><span class="iconfont">&#xe661;</span><span class="school"> 扬州大学信息工程学院</span></li><li><span class="iconfont">&#xec70;</span><span> 河南郑州</span></li><li><span class="iconfont">&#xe76b;</span><span class="like"> 看侦探小说</span></li></ul></div></div></div>
    <div class="right"><div class="content"><div></div></div></div>
  </div>
</template>

<script>
export default {
  name: 'myheadtop',
}
</script>
<style lang="stylus" scoped>
.head
  width 88%
  margin 0 auto
  display flex
  justify-content space-around
  .left,.right
    padding-top 50px
    width 40%
    height 0
    padding-bottom 60%
    background linear-gradient(135deg,#f8e2a2 88%,white 88.5%)
    position relative
    &:after
      position absolute
      right 0
      bottom 0
      display block
      content ''
      width 31.5%
      padding-bottom 31.5% 
      background linear-gradient(135deg,#967f3c 50%,white 50%)
    .content
      width 75%
      height 0
      padding-bottom 115%
      margin 0 auto
      overflow hidden
      li
        margin-bottom 3px
        padding-bottom 3px
        border-bottom dashed 1px red
        span 
          font-size 3.5vw
        .iconfont
          font-size 5vw
        .school 
          font-size 2vw
        .like
          font-size 3.5vw
      

      

  
</style>
