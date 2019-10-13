<template>
  <div>
    <div class='weekend-title'>周末去哪儿</div>
    <ul class="weekend-content">
      <li v-for="(item,index) of weekendList" :key="index">
        <div class="weekend-img">
          <img class="weekend-img-content" :src="item.imgUrl"/>
        </div>
        <div class="weekend-bottom">
          <div class="weekend-intro">{{item.intro}}</div>
          <div class="weekend-detail">{{item.desc}}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  },
  data () {
    return {}
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixins.styl';

  .weekend-title
    margin-top: .1rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .weekend-content
      display: flex
      flex-direction: column
      .weekend-img
        height: 0
        padding-bottom: 37.5%
        overflow: hidden
        .weekend-img-content
          width: 100%
      .weekend-bottom
        padding-top: .2rem
        padding-left: .2rem
        padding-right: .2rem
        padding-bottom: .2rem
        .weekend-intro
          color: #212121
          font-size: .28rem
          line-height: .48rem
        .weekend-detail
          color: #616161
          font-size: .24rem
          line-height: .42rem
</style>
