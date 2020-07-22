<template>
  <div class="home1 border-bottom">
    <headtop></headtop>
    <div class="home2"><div class="swiper-paginationhome" slot="pagination"></div></div>
    <swiper :options="swiperOptions" class="home">
      <swiper-slide>
    <headattach></headattach>
   <headtool></headtool>
   <headlist></headlist>
   <headtoutiao></headtoutiao>
  <div class="content"></div>
  </swiper-slide>
  <swiper-slide>

   <div class="content"></div>
  </swiper-slide>
  
  </swiper>
  </div>
</template>

<script>
import headtop from './components/header'
import headattach from './components/main'
import headtool from './components/sidebar'
import headlist from './components/songlist'
import headtoutiao from './components/bottom'
export default {
  name: 'Home',
  components: {
    headtop,
    headattach,
    headtool,
    headlist,
    headtoutiao
  },
  data () {
    return {
      swiperOptions: {
        autoplay:false,
        pagination: '.swiper-paginationhome' //防止页面中两个swiper组件下的原点导航条冲突所以后面加一
      }
    }
  }
}
</script>
<style lang="stylus" scoped>

.home2 >>> .swiper-pagination-bullet
  border-radius 0
  width 16px
  height 4px
  overflow hidden
  float left
  margin-left 8vw
  background lightblue
  border-radius 30%
.home2 >>> .swiper-pagination-bullet:nth-child(2)
  margin-left 18vw
.home2 >>> .swiper-pagination-bullet-active
  background white
  
.content
  height 700px
  width 100%
.home2
  position fixed
  z-index 101
  left 0
  right 0
  height 8px
  padding-top 35px

  

</style>