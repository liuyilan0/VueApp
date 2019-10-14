<template>
  <div>
    <router-link tag="div" class="header-abs" v-show="!showNavigation" to="/">>
      <span class="iconfont header-back">&#xe613;</span>
    </router-link>
    <div class="header-fixed" v-show="showNavigation">
      <span class="iconfont header-fixed-back">&#xe613;</span>景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailNavigation',
  data () {
    return {
      showNavigation: false
    }
  },
  methods: {
    handleScroll () {
      const scrollTop = document.documentElement.scrollTop || document.body.scrollTop || window.pageYOffset
      if (scrollTop > 60) {
        this.showNavigation = true
      } else {
        this.showNavigation = false
      }
    }
  },

  activated () {
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/variable.styl'
  .header-abs
    position: absolute
    left: .2rem
    top: .2rem
    width: .8rem
    height: .8rem
    line-height: .8rem
    border-radius: .4rem
    background: rgba(0, 0, 0, 0.8)
    text-align: center
    .header-back
      color: #fff
      font-size: .4rem
  .header-fixed
    position: fixed
    top: 0
    left: 0
    right: 0
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    text-align: center
    font-size: .32rem
    .header-fixed-back
      position: absolute
      top: 0
      left: 0
      width: .64rem
      color: #fff
</style>
