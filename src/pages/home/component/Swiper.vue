<template>
  <div class="swiper-wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide
        v-for="item in swiperList"
        :key="item.id"
      >
        <img class="swiper-img" :src="item.url" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HeaderSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        url: 'http://www.bwgsd.com/data/upload/mobile/special/s0/s0_20180530173438.jpg'
      }, {
        id: '002',
        url: 'http://www.bwgsd.com/data/upload/mobile/special/s0/s0_05696896038449284.jpg'
      }, {
        id: '003',
        url: 'http://www.bwgsd.com/data/upload/mobile/special/s0/s0_05696895672812879.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper-wrapper >>> .swiper-pagination-bullet-active
    background #46587C
  .swiper-wrapper
    .swiper-img
      width 100%
</style>
