<template>
<div class="head">
<div class="headtitle">
     <span class="iconfont">&#xe61b;</span>
     <span>音乐日历</span>
     <transition>
     <div class="content" v-if="show"><span class="date">{{datacontent.date}}</span><br><br><p><span class="wenzi">{{datacontent.content}}</span></p></div>
     </transition>
</div>    
</div>
</template>
<script>
export default {
  name: 'toutiao',
  data () {
      return {
          show: true,
          datalist: [{
            date: '07-25',
            content: '今日火星陨落'
          }
          ,{
            date: '07-26',
            content: '今日水星陨落'
          },{
            date: '07-27',
            content: '今日冥王星陨落'
           }],
           datacontent: {
            date: '',
            content: ''
          }
           
           
      }},
      computed: {
    len () {
      return this.datalist.length
    }
  },
  mounted () {
    var x =0
    let y = 0 
    const that = this  //进入setimeout后this的指向会丢失所以在闭包内用that记住this
    if(this.datalist[0])
    {this.datacontent = this.datalist[0]
    }
    var f=setTimeout(function h () {//之前的困难时消失的时间和出现的时间一样但是我想要的效果是出现的时间（5s）大于消失的时间(1s)
    
    if(y==that.len){
      y = 0
    }
    if(that.show)//执行第一次h函数时候that.show==true因为这个show是我在data最先定义过的
    {
      y++
      that.show = !that.show//第一次时候变为false消失
      setTimeout(h,500)//控制从消失到出现的间隔时间,进入第二个h函数它负责将数据转换到datalist[1]并且show被变为true
    }else{
     that.datacontent = that.datalist[y]
     that.show= !that.show
     setTimeout(h,5000)//控制持续时间
    }
    }
    ,5000)
    
}
}
      
      
</script>
<style lang="stylus" scoped>
.head
  width 88%
  margin 0 auto
  margin-top 5%
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
.v-enter, .v-leave-to 
	opacity 0
.v-enter-active, .v-leave-active
  transition opacity 500ms
</style>
