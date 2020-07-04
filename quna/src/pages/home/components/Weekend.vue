<template>
  <div>
    <div class="title">周末去哪玩</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data: function () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '北京欢乐谷',
        desc: '亚洲唯一飞行式过山车等你来挑战'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
        title: '北京野生动物园',
        desc: '敢与森林之王近距离接触吗？'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title: '故宫',
        desc: '世界五大宫之首，穿越与您近在咫尺'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixings.styl'
  .title
    margin-top:.2rem
    line-height :.8rem
    background :#eee
    text-indent :.2rem
  .item-img-wrapper
    overflow :hidden
    height :0
    padding-bottom :33.9%
  .item-img
      width:100%
   .item-info
      padding:.1rem
  .item-title
    line-height :.54rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height :.4rem
    color:#ccc
    ellipsis()
</style>
