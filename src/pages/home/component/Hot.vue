<template>
  <div class="hot">
    <div class="hot-header">
      热
    </div>
    <div ref="listWrapper">
      <ul class="hot-list">
        <li class="hot-img-wrapper slider-item" v-for="item in hotList" :key="item.id">
          <img class="hot-img" :src="item.url" />
          <p class="hot-item-desc">{{item.desc}}</p>
          <p class="hot-item-price">￥{{item.price}}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'Homehot',
  data () {
    return {
      hotList: [{
        id: '001',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }, {
        id: '002',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }, {
        id: '003',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }, {
        id: '004',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }, {
        id: '005',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }, {
        id: '006',
        url: '../../../../static/mock/2_05271971343721616.jpg',
        desc: '体育馆运动纪念品迷你足球篮球排球棒球钥匙扣挂件小礼品',
        price: '9'
      }]
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.listWrapper, {
      scrollY: false,
      scrollX: true,
      bounce: false
    })
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .hot
    padding 10px 0
    border-bottom 5px solid #eee
    .hot-header
      position relative
      margin 0 auto
      width 1rem
      height 1rem
      border .1rem solid #46587C
      border-radius 1rem
      text-align center
      line-height 1rem
      font-size .6rem
    .hot-list
      width 18rem
      overflow hidden
      .hot-img-wrapper
        width 3rem
        float left
        .hot-img
          width 100%
        .hot-item-desc
          ellipsis()
        .hot-item-price
          color red
</style>
