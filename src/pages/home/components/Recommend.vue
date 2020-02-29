<template>
  <div>
    <div class="title">
    热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p calss="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/2001/f6/f66fb64d494a4d78a3.img.jpg_200x200_005ebaf5.jpg',
        title: '上海海昌海洋公园',
        desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/2001/f6/f66fb64d494a4d78a3.img.jpg_200x200_005ebaf5.jpg',
        title: '上海海昌海洋公园',
        desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/2001/f6/f66fb64d494a4d78a3.img.jpg_200x200_005ebaf5.jpg',
        title: '上海海昌海洋公园',
        desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
   .item
      display: flex
      height: 1.9rem
      overflow: hidden
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: 0.1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        ellipse()
        line-height: .54rem
        font-size: .32rem
      .item-desc
        ellipse()
        line-height: .4rem
        color: #ccc
      .item-button
        line-height: .44rem
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
        margin-top: .16rem
        color: #fff
</style>
