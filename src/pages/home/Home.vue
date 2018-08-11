<template>
  <div>
    <home-header></home-header>
    <header-swiper></header-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HeaderSwiper from './component/Swiper'
import HomeIcons from './component/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HeaderSwiper,
    HomeIcons
  }
}
</script>

<style lang="stylus" scoped>

</style>
