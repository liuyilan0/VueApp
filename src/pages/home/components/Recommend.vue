<template>
  <div>
    <div class='recommend-title'>推荐景点</div>
    <ul>
      <li v-for="item in recommendList" :key='item.id' class='recommend-item-view'>
        <img class="recommend-img" :src="item.imgUrl"/>
        <div class="recommend-content">
          <p class="item-name">{{item.title}}</p>
          <p class="item-level">
            <span class="item-star-view">
              <span v-for="(star, index) in Number(item.level)" :key="index" class="item-star"></span>
            </span>
            <span class="item-comment">{{item.comment}}条评论</span>
          </p>
          <p class="item-bottom">
            <span class="item-price-left">¥</span>
            <span class="item-price">{{item.price}}</span>
            <span class="item-price-right">起</span>

            <span class="item-place">{{item.place}}</span>
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  },
  data () {
    return {}
  }
}
</script>

<style lang='stylus' scoped>
@import 'http://netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css';

  .recommend-title
    margin-top: .1rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .recommend-item-view
    display: flex
    overflow: hidden
    height: 2.0rem
    padding: .1rem
    .recommend-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .recommend-content
      flex: 1
      padding: .2rem
      .item-name
        font-size:.22rem
        line-height: .54rem
      .item-level
        font-size: .22rem
        line-height: .48rem
        .item-star-view
          color: orange
          .item-star:before
            content: '\f005';
            font-family: FontAwesome;
        .item-comment
          margin-left: .2rem
      .item-bottom
        line-height: .56rem
        .item-price-left
          font-size: .20rem
          color: orange
          font-weight: 900
        .item-price
          font-size:.36rem
          color: orange
          font-weight: 900
        .item-price-right
          font-size: .20rem
        .item-place
          float:right
          font-size:.22rem
</style>
