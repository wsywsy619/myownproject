<template>
  <div class="home border-bottom">
   <headtop></headtop> 
  <div class="content"></div>
  </div>
</template>

<script>
import headtop from './components/header'
export default {
  name: 'Home',
  components: {
    headtop
  }
}
</script>
<style lang="stylus" scoped>
.content
  height 700px
  width 100%
</style>
