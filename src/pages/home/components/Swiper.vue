<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for="item of imgList" :key="item.id">
        <img class="swiper-image" :src="item.imgUrl"><img>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    imgList: Array
  },
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 2000
      }
    }
  },
  computed: {
    // 当数据加载出来以后再创建，否则swiper会默认展示最后一条数据
    showSwiper () {
      return this.imgList.length
    }
  }
}
</script>

<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    height: 0
    width: 100%
    padding-bottom: 26.66%    /** 高/宽的比例 */
    background: #eee
    .swiper-image
      width: 100%
</style>
