<template>
  <div class="container" @click="handleClickGallary">
    <div class="wrapper">
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(item,index) of imgList" :key="index">
          <img class="wrapper-img" :src="item"/>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailGallary',
  props: {
    imgList: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleClickGallary () {
      this.$emit('close')
    }
  }
}
</script>

<style lang='stylus' scoped>
  .container >>> .swiper-container
    overflow: inherit
  .container
    display: flex
    flex-direction: column
    justify-content: center
    position: fixed
    top: 0
    left: 0
    right: 0
    bottom: 0
    background: #000
    .wrapper
      height: 0
      width: 100%
      padding-bottom: 66%
      .wrapper-img
        width: 100%
      .swiper-pagination
        bottom: -1rem
</style>
