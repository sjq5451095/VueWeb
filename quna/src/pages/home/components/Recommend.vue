<template>
  <div>
     <div class="title">热销推荐</div>
     <ul>
       <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <img class="item-img" :src="item.imgUrl" alt="">
            <div class="item-info">
               <p class="item-title">{{item.title}}</p>
               <p class="item-desc">{{item.desc}}</p>
               <button class="item-button">查看详情</button>
            </div>
       </li>
     </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data: function () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1911/29/29d9b9078000774fa3.img.jpg_200x200_3621a35a.jpg',
        title: '北京欢乐谷',
        desc: '亚洲唯一飞行式过山车等你来挑战'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
        title: '北京野生动物园',
        desc: '敢与森林之王近距离接触吗？'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
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
    .item
      display :flex
      height: 1.9rem
      overflow :hidden
    .item-img
      width:1.7rem
      height:1.7rem
      padding:.1rem
    .item-info
      flex:1
      padding:.1rem
      min-width: 0
      .item-title
        line-height :.54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height :.4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height :.44rem
        background :#ff9200
        padding: 0 .2rem
        border-radius :.06rem
        margin-top :.3rem
        color :#fff
</style>
