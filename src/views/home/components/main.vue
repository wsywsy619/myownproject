<template>
  <div class="head">
    <div class="headyifu">
    <swiper :options="swiperOptions" class="wert">
    <swiper-slide><img src="http://p1.music.126.net/7pxwS_nmTjacpBgYrCbLIA==/109951165140301808.jpg?imageView&quality=89" alt="diyi"></swiper-slide>
    <swiper-slide><img src="http://p1.music.126.net/5AZy9EMcvjN4HZggWSb0Nw==/109951165141849316.jpg?imageView&quality=89" alt="dier"></swiper-slide>
    <swiper-slide><img src="http://p1.music.126.net/baWhRWaAzB7_gQz_U4F4kA==/109951165141423818.jpg?imageView&quality=89" alt="disan"></swiper-slide>
    <swiper-slide><img src="http://p1.music.126.net/5hORw5NpVhLkI1P0G1_BXg==/109951165141924449.jpg?imageView&quality=89" alt="disi"></swiper-slide>
    <swiper-slide><img src="http://p1.music.126.net/rB9TVBGueV9aFveF-00_fw==/109951165142399033.jpg?imageView&quality=89" alt="diwu"></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
  </div>
</template>
<script>
export default {
  name: 'headattach',
  data() {
      return {
        swiperOptions: {
          pagination: '.swiper-pagination',
          loop: true,
          autoplay : 5000, //设置自动播放并且设置间隔时间
          autoplayDisableOnInteraction: false//在干扰转动的时候是否能够继续转动下去
        }
      }
    }
}
</script>
<style lang="stylus" scoped>
.headyifu >>> .swiper-pagination-bullet-active
  background-color white 
.head
  width 100%
  height 100%
  background lightblue
  border-bottom-right-radius 25px
  border-bottom-left-radius 25px
  touch-action: none /*用于解决加入vueawesomeswipeIgnored attempt to cancel a touchmove event with cancelable=false, for example because scrolling is */ 
  .headyifu
    width 88%
    background ivory
    position relative
    bottom -85px
    left 50%
    margin-left -44%
    border-radius 13px
    overflow hidden
    position: relative /*relative与 z-index 用于解决手机上overflow hidden 失效的问题 */
    z-index 1
    box-shadow 10px -10px 3px #888888;
    img  
      width 100%
</style>
