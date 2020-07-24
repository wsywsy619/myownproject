<template>
<div class="head">
<div><span class="iconfont">&#xe61c;</span><div>rank</div></div><div><span class="iconfont">&#xe74e;</span><div>comet</div></div><div><span class="iconfont">&#xe67b;</span><div>ilike</div></div><div><span class="iconfont">&#xe67c;</span><div>Mylist</div></div><div><span class="iconfont">&#xe60a;</span><div>CD</div></div>
</div>
</template>
<script>
export default {
  name: 'headattach'
}
</script>
<style lang="stylus" scoped>
.head
  width 100%
  margin-top 80px
  display flex
  div
    width 25%
    text-align center
    color lightblue
    span 
      font-size 14vw
      &+div
        width 100%
        font-size 5vw
</style>
