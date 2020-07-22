<template>
  <div class="head">
    <div class="head1" :class="{'colordisplay':display}">
    <div class="shou" :class="{'colordisplay1':display}">首页</div>
    <div class="wode" :class="{'colordisplay1':display}">我的音乐</div>
    <div class="icon"><span class="iconfont" :class="{'colordisplay1':display}">&#xe61d;</span></div>
   </div>
  </div>
</template>

<script>
export default {
  name: 'headtop',
  data () {
    return {
      display: false,
      colorfg: "green"
    }
  },
  methods: {
    handlescroll () {
      var top= document.documentElement.scrollTop
      if(top)
      {
        this.display= true
      }
      else
      {
         this.display =false
      }
    }
  }
  ,mounted () {
    window.addEventListener('scroll', this.handlescroll)
  }

}
</script>
<style lang="stylus" scoped>
.colordisplay
  background #ffffff
  border-bottom solid 1px #d6d2d1
  .colordisplay1
    color lightblue

    
.head
  position fixed
  left 0
  right 0
  height 40px
  z-index 100
  background lightblue 
  border-bottom solid 1px lightblue
  .head1
    display flex 
    justify-content space-between
    color #fff
    .shou
      width 20%
      padding-left 7vw
      line-height 40px
      font-size 20px
      position relative
    .wode
      font-size 19px
      text-align left
      line-height 40px
      width 70%
    .icon
      width 10%
      text-align center
      line-height 40px
</style>
