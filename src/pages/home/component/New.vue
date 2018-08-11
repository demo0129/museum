<template>
  <div class="new">
    <div class="new-header">
      新
    </div>
    <div ref="newlistWrapper">
      <ul class="new-list">
        <li class="new-img-wrapper slider-item" v-for="item in newList" :key="item.id">
          <img class="new-img" :src="item.url" />
          <p class="new-item-desc">{{item.desc}}</p>
          <p class="new-item-price">￥{{item.price}}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'HomeNew',
  data () {
    return {
      newList: [{
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
    this.scroll = new Bscroll(this.$refs.newlistWrapper, {
      scrollY: false,
      scrollX: true,
      bounce: false
    })
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .new
    padding 10px 0
    border-top 5px solid #eee
    border-bottom 5px solid #eee
    .new-header
      position relative
      margin 0 auto
      width 1rem
      height 1rem
      border .1rem solid #46587C
      border-radius 1rem
      text-align center
      line-height 1rem
      font-size .6rem
    .new-list
      width 18rem
      overflow hidden
      .new-img-wrapper
        width 3rem
        float left
        .new-img
          width 100%
        .new-item-desc
          ellipsis()
        .new-item-price
          color red
</style>
