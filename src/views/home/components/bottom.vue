<template>
<div class="head">
<div class="headtitle">
     <span class="iconfont">&#xe61b;</span>
     <span>音乐日历</span><button @click="handleclick">显示</button>
     <transition type="transition" appear appear-active-class="animate__animated animate__bounce" enter-active-class="v-enter-active" leave-active-class="v-leave-active">
     <div class="content" v-if="show"><span class="date">07-25</span><br><br><p><span class="wenzi">今日火星陨落</span></p></div>
     </transition>
</div>    
</div>
</template>
<script>
export default {
  name: 'toutiao',
  data () {
      return {
          show: true
      }
  },
  methods: {
      handleclick () {
          this.show = !this.show
      }
  }
}
</script>
<style lang="stylus" scoped>
.head
  width 88%
  margin 0 auto
  margin-top 33%
  height 0
  padding-bottom 30%
  border solid 1px #EAEAEA	
  box-shadow: 1px 1px 3px .5px #EAEAEA	 
  border-radius 15px
  .headtitle
    padding-top 2%
    padding-left 2%
    color lightblue
  .iconfont
    font-size 5vw
    font-weight bolder
    +span 
      font-size 5vw
  .content
    margin-top 5%
    .date
      color black
      font-size 4vw
    p
      text-indent 20px
      .wenzi
        color #9E9E9E
        font-size 4vw
        text-indent 100px
.v-enter,.v-leave-to 
	opacity 0
.v-enter-active,.v-leave-active
	transition opacity 5s
</style>
