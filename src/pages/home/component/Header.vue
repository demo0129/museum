<template>
  <div>
    <div class="header-wrapper">
        <div class="seller-img"></div>
      <div class="seller-function">
        <div class="guanzhu"
             @click="handleClickGuan"
             :class="{'guan-active': guanChange}"
        >{{guanText}}
        </div>
        <div class="qiandao" @click="qianHide" v-if="qianShow">签到</div>
      </div>
    </div>
    <div class="guanzhu-wrapper" v-show="guanShow" >
      <transition enter-active-class="animated zoomIn">
        <div
          class="guanzhu-desc"
          ref="guanzhuDesc"
          v-show="guanShow"
        >
        <p>关注成功</p>
        <p>宣传语或者是关注后想显示的活动</p>
        <span
          class="close-btn iconfont"
          @click="closeGuan"
        >&#xe628;
        </span>
      </div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      guanText: '关注',
      guanChange: false,
      guanShow: false,
      qianShow: true
    }
  },
  methods: {
    handleClickGuan () {
      this.guanChange = !this.guanChange
      if (this.guanChange) {
        this.guanShow = true
        this.guanText = '取消关注'
      } else {
        this.guanText = '关注'
      }
    },
    closeGuan () {
      this.guanShow = false
    },
    qianHide () {
      this.qianShow = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .header-wrapper
    display flex
    align-items center
    height .7rem
    padding .2rem
    .seller-img
      width 40%
      height 100%
      background-size 100% 100%
      background-image url("museum.jpg")
      background-repeat:no-repeat
    .seller-function
      flex 1
      display flex
      justify-content flex-end
      .guanzhu
        padding .1rem .26rem .1rem .3rem
        border 1px solid #46587C
        border-radius .24rem
        margin-right .3rem
        color #ffffff
        background #46587C
        letter-spacing .04rem
        font-size .24rem
        &.guan-active
          color #46587C
          background #ffffff
      .qiandao
        padding .1rem .26rem .1rem .3rem
        border 1px solid #46587C
        border-radius .24rem
        color #46587C
        background #ffffff
        letter-spacing .04rem
        font-size .24rem
  .guanzhu-wrapper
    z-index 50
    position fixed
    top 0
    right 0
    left 0
    bottom 0
    background rgba(0,0,0,.5)
    display flex
    justify-content center
    align-items center
    .guanzhu-desc
      position relative
      width 5rem
      height 10rem
      padding .2rem
      background #fff
      animation-duration 0.2s
      .close-btn
        position absolute
        bottom .2rem
        right 50%
        font-size .6rem
</style>
