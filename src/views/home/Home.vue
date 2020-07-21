<template>
  <div class="home border-bottom">
    <headtop></headtop>
    <swiper :options="swiperOptions">
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
            autoplay:false
          }}
  }
}
</script>
<style lang="stylus" scoped>
.content
  height 700px
  width 100%
</style>
