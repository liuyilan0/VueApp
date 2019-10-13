<template>
   <div class="header">
    城市选择
    <router-link to="/">
      <span class="iconfont headerback">&#xe613;</span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang='stylus' scoped>
@import '~styles/variable.styl'
  .header
    overflow: hidden
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    text-align: center
    font-size: .32rem
    .headerback
      position: absolute
      top: 0
      left: 0
      width: .64rem
      color: #fff
</style>
