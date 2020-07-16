<template>
  <div class="head">
    <div class="headtitle">
     <div>看看最新歌单</div>
     <button @click="handleclick">查看更多</button> 
    </div>
    <div class="wrapper">
        <div class="icon"><div class="iconimage"><img src="http://p2.music.126.net/RRFu6VeRuBH6Cbbi30_L6A==/109951164923240340.jpg?param=140y140" alt="first"><p>我的奇妙小姐【声控馆】</p></div></div>
        <div class="icon"><div class="iconimage"><img src="http://p2.music.126.net/IL9MOW1GfETCmKZ8UhLDLA==/109951165137654443.jpg?param=140y140" alt="second"><p>翻唱辑｜华语宝藏Cover精选</p></div></div>
        <div class="icon"><div class="iconimage"><img src="http://p2.music.126.net/VPh2ZbbSNRC2fDUivIXN5Q==/109951165005302772.jpg?param=140y140" alt="third"><p>黑眼圈，是每天夜晚心事的落款</p></div></div>
        
    </div>
  </div>
</template>

<script>
export default {
  name: 'headtop',
  methods: {
      handleclick () {
          alert('hello')
      }
  }
}
</script>
<style lang="stylus" scoped>
.head
  width 88%
  margin 0 auto
  height 35px
  border-bottom solid 3px lightblue
  .headtitle
    height 22px
    div
      color lightblue
      float left
      font-size 22px
      font-weight 550
    button
      float right
      padding 1px 13px
      border-radius 15px
      border solid 1px #ccc
      background white
  .wrapper
    margin-top 35px
    width 100%
    height 0
    padding-bottom 33%
    .icon
      width 33%
      padding-bottom 170px
      float left
      position relative
      .iconimage
        position absolute 
        left 0
        top 0
        right 0
        bottom 20px
        p
          width 80%
          font-size 12px
          overflow hidden
          white-space: nowrap
          text-overflow: ellipsis
        img 
          width 80%
          border-radius 10px

</style>
