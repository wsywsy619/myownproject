<template>
  <div class="head">
    <div class="left"><div class="content"><div><p>我的列表</p><p>我的列表</p><p>我的列表</p><p>我的列表</p></div></div></div>
    <div class="right"><div class="content"><div><p>看看bier</p></div></div></div>
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
      padding-bottom 115%
      margin 0 auto
      div
        position absolute
      

  
</style>
