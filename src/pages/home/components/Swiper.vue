<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
    <swiper-slide v-for="item of imgList" :key="item.id">
      <img class="swiper-image" :src="item.img"><img>
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      imgList: [
        { 'id': '1',
          'img': 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/78b240572657a6da67e662540c846dd6.jpg_750x200_b75c8be9.jpg'
        },
        { 'id': '2',
          'img': 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/06e65ace8dce3638e847b04e975489d1.jpg_750x200_a2dcb0a4.jpg'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
  .swiper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow:hidden
    height:0
    width: 100%
    padding-bottom:31.25%    /** 高/宽的比例 */
    .swiper-image
      width: 100%
</style>
