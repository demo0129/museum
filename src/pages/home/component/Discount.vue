<template>
  <div class="dis">
    <div class="dis-header">
      热
    </div>
    <div ref="dislistWrapper">
      <ul class="dis-list">
        <li class="dis-img-wrapper slider-item" v-for="item in disList" :key="item.id">
          <img class="dis-img" :src="item.url" />
          <p class="dis-item-desc">{{item.desc}}</p>
          <p class="dis-item-price">￥{{item.price}}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'HomeDis',
  data () {
    return {
      disList: [{
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
    this.scroll = new Bscroll(this.$refs.dislistWrapper, {
      scrollY: false,
      scrollX: true,
      bounce: false
    })
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .dis
    padding 10px 0
    border-bottom 5px solid #eee
    .dis-header
      position relative
      margin 0 auto
      width 1rem
      height 1rem
      border .1rem solid #46587C
      border-radius 1rem
      text-align center
      line-height 1rem
      font-size .6rem
    .dis-list
      width 18rem
      overflow hidden
      .dis-img-wrapper
        width 3rem
        float left
        .dis-img
          width 100%
        .dis-item-desc
          ellipsis()
        .dis-item-price
          color red
</style>
