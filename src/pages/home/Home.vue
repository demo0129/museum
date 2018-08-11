<template>
  <div>
    <home-header></home-header>
    <header-swiper></header-swiper>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HeaderSwiper from './component/Swiper'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HeaderSwiper
  }
}
</script>

<style lang="stylus" scoped>

</style>
