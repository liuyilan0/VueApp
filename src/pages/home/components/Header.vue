<template>
  <div class="container">
    <div class="header-left">
      <span class="iconfont">&#xe613;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe600;</span>
      <span class="input">输入城市/景点/游玩主题</span>
    </div>
    <router-link tag="div" to="/city" class="header-right">
        <span class="city">{{city}}</span>
        <span class="iconfont">&#xe607;</span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variable.styl'
  .container
    display: flex
    line-height:$headerHeight
    background:$bgColor
    color: #fff
    .header-left
      float:left
      width:.4rem
      margin-left:.2rem
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
      .input
        margin-left:.1rem
        font-size: .26rem
    .header-right
      float:right
      width:1.24rem
      text-align:center
      color: #fff
      .city
        font-size: .26rem
</style>
