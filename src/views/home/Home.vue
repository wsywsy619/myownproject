<template>
  <div class="home border-bottom">
   <headtop></headtop>
   <headattach></headattach>
   <headtool></headtool>
   <headlist></headlist>
   <headtoutiao></headtoutiao>
  <div class="content"></div>
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
  }
}
</script>
<style lang="stylus" scoped>
.content
  height 700px
  width 100%
</style>
