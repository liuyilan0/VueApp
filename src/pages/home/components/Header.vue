<template>
  <div class="container">
    <div class="header-left">
      <span class="iconfont">&#xe613;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe600;</span>欢迎使用
    </div>
    <div class="header-right">
      城市<span class="iconfont">&#xe607;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variable.styl'
  .container
    display: flex
    line-height:.86rem
    background:$bgColor
    color: #fff
    .header-left
      float:left
      width:.64rem
    .header-input
      flex:1
      background:#fff
      border-radius:.1rem
      margin-top:.12rem
      margin-left:.2rem
      padding-left: .2rem
      height:.64rem
      line-height:.64rem
      color:#ccc
      text-align:left
    .header-right
      float:right
      width:1.24rem
      text-align:center
</style>
