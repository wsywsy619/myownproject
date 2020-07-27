<template>
  <div class="head">
    <div class="left"><div class="content"><div><ul><li><div><span class="iconfont">&#xe602;</span><p>姓名</p></div><span> 魏思远</span></li><li><div><span class="iconfont">&#xe619;</span><p>年龄</p></div><span> 21</span></li><li><div><span class="iconfont">&#xe661;</span><p>学校</p></div><span class="school"> 扬州大学信息工程学院</span></li><li><div><span class="iconfont">&#xe76b;</span><p>爱好</p></div><span class="like"> 看侦探小说</span></li></ul></div></div></div>
    <div class="right"><div class="content"><div><ul><li><div><span class="iconfont">&#xe600;</span><p>粉丝</p></div><span> 3</span></li><li><div><span class="iconfont">&#xe612;</span><p>关注</p></div><span> 20</span></li><li><div><span class="iconfont">&#xe631;</span><p>歌单</p></div><span> 5</span></li><li><div><span class="iconfont">&#xe625;</span><p>留言</p></div><span> 7</span></li></ul></div></div></div>
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
        div
          display inline-block
          span
            font-size 5vw
          p
            font-size 2.3vw
            text-align center
          &+span
            display inline-block
            position relative
            top -1vw
            left 1vw
            font-size 5vw
        .school,.like
          font-size 3vw
          overflow hidden
          white-space: nowrap
          text-overflow: ellipsis
          width 70%
        
      

      

  
</style>
