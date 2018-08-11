<template>
  <div>
    <home-header></home-header>
    <header-swiper></header-swiper>
    <home-icons></home-icons>
    <home-new></home-new>
    <home-hot></home-hot>
    <home-dis></home-dis>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HeaderSwiper from './component/Swiper'
import HomeIcons from './component/Icons'
import HomeHot from './component/Hot'
import HomeNew from './component/New'
import HomeDis from './component/Discount'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HeaderSwiper,
    HomeIcons,
    HomeHot,
    HomeNew,
    HomeDis
  }
}
</script>

<style lang="stylus" scoped>

</style>
