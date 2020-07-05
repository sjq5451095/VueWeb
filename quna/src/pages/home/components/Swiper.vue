<template>
  <div class="wraper">
    <swiper :options="swiperOption"  v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-image" :src="item.imgUrl" >
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      // 解决轮播首次加载顺序bug
      return this.list.length
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
