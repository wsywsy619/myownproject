<template>
  <div class="head">
    <div class="headtitle">
     <div>看看最新歌单</div>
     <button @click="handleclick">查看更多</button> 
    </div>
    <div class="wrapper">
        <swiper>
        <swiper-slide v-for="(item1,index) of pages" :key="index">
        <div class="icon" v-for="item of item1" :key="item.id"><div class="iconimage"><img :src="item.imgurl" :alt="item.id"><p>{{item.des}}</p></div></div>
        </swiper-slide>
        </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'headtop',
  methods: {
      handleclick () {
        console.log(this.pages.length)
      }
  },
  data () {
    return {
      iconlist: [{
        id: '0001',
        imgurl: 'http://p2.music.126.net/RRFu6VeRuBH6Cbbi30_L6A==/109951164923240340.jpg?param=140y140',
        des: '我的奇妙小姐【声控馆】'
      }, 
      {
        id: '0002',
        imgurl: 'http://p2.music.126.net/IL9MOW1GfETCmKZ8UhLDLA==/109951165137654443.jpg?param=140y140',
        des: '翻唱辑｜华语宝藏Cover精选'
      },
      {
        id: '0003',
        imgurl: 'http://p2.music.126.net/RRFu6VeRuBH6Cbbi30_L6A==/109951164923240340.jpg?param=140y140',
        des: '我的奇妙小姐【声控馆】'
      }, 
      {
        id: '0004',
        imgurl: 'http://p2.music.126.net/IL9MOW1GfETCmKZ8UhLDLA==/109951165137654443.jpg?param=140y140',
        des: '翻唱辑｜华语宝藏Cover精选'
      },
      {
        id: '0005',
        imgurl: 'http://p2.music.126.net/RRFu6VeRuBH6Cbbi30_L6A==/109951164923240340.jpg?param=140y140',
        des: '我的奇妙小姐【声控馆】'
      }, 
      {
        id: '0006',
        imgurl: 'http://p2.music.126.net/IL9MOW1GfETCmKZ8UhLDLA==/109951165137654443.jpg?param=140y140',
        des: '翻唱辑｜华语宝藏Cover精选'
      },
      {
        id: '0007',
        imgurl: 'http://p2.music.126.net/RRFu6VeRuBH6Cbbi30_L6A==/109951164923240340.jpg?param=140y140',
        des: '我的奇妙小姐【声控馆】'
      }, 
      {
        id: '0008',
        imgurl: 'http://p2.music.126.net/IL9MOW1GfETCmKZ8UhLDLA==/109951165137654443.jpg?param=140y140',
        des: '翻唱辑｜华语宝藏Cover精选'
      }]
    }
  },
  computed: {
    pages () {
      const pages =[]
      this.iconlist.forEach((item, index) => {
        if(!pages[parseInt(index/3)]) {
          let y = []
          y.push(item)
          pages.push(y)
        }else{
          pages[parseInt(index/3)].push(item)
        }
        })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
.head
  width 88%
  margin 2% auto
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
    overflow hidden
  .wrapper >>> .swiper-container
    height 0
    padding-bottom 33%
    .icon
      width 33%
      padding-bottom 170px
      float left
      position relative
      .iconimage
        position absolute 
        left 10%
        top 0
        right 0
        bottom 20px
        p
          width 80%
          font-size 2.5vw
          overflow hidden
          white-space: nowrap
          text-overflow: ellipsis
        img 
          width 80%
          border-radius 10px

</style>
