<template>
  <div>
    <div class="item" v-for="(item, index) of dataList" :key="index">
      <div class="parents border-bottom">
        <span class="icon"></span>
        <span class="title">{{item.title}}</span>
      </div>
      <div v-if="item.children" class="children">
        <detail-list :dataList='item.children'></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    dataList: Array
  }
}
</script>

<style lang='stylus' scoped>
    .item
      background: #fff
      .parents
        .icon
          display: inline-block;
          position: relative;
          width: .36rem;
          height: .36rem;
          top: .1rem;
          left: .12rem;
          background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
          margin-right: .1rem;
          background-size: .4rem 3rem;
        .title
          font-size: .30rem
          line-height: .8rem
          padding: 0 .1rem
      .children
        padding: 0 .2rem

</style>
