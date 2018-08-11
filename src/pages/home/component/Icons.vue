<template>
  <div>
    <ul class="icon-list">
      <li class="icon-item">
        <span class="iconfont icon">&#xe601;</span>
        <p class="icon-info">食</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe600;</span>
        <p class="icon-info">包</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe620;</span>
        <p class="icon-info">居</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe6a7;</span>
        <p class="icon-info">公</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe63d;</span>
        <p class="icon-info">饰</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe634;</span>
        <p class="icon-info">瓷</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe614;</span>
        <p class="icon-info">书</p>
      </li>
      <li class="icon-item">
        <span class="iconfont icon">&#xe61f;</span>
        <p class="icon-info">音</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  .icon-list
    overflow hidden
    margin .4rem auto
    width 90%
    .icon-item
      box-sizing border-box
      text-align: center
      width 25%
      float left
      padding .3rem
      .icon
        font-size .7rem
</style>
