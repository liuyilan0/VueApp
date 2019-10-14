<template>
  <div>
    <detail-header></detail-header>
    <detail-navigation></detail-navigation>
    <div class="bottom"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailNavigation from './components/Navigation'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailNavigation
  }
}
</script>

<style lang='stylus' scoped>
  .bottom
    height: 50rem
</style>
