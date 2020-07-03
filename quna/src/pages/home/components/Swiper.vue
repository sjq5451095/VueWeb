<template>
  <div class="wraper">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-image" :src="item.imgUrl" >
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: '../../../../static/FO7A9244.jpg'
      }, {
        id: '002',
        imgUrl: '../../../../static/FO7A9251.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
      .wraper >>> .swiper-pagination-bullet-active
        background :#fff
      .wraper
        width:100%
        height: 0
        overflow :hidden
        padding-bottom :31.25%
      .swiper-image
       width:100%
       height:2.5rem
</style>
