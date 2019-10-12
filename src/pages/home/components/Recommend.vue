<template>
  <div>
    <div class='recommend-title'>推荐景点</div>
    <ul>
      <li v-for="item in recommendList" :key='item.id' class='recommend-item-view'>
        <img class="recommend-img" :src="item.imgUrl"/>
        <div class="recommend-content">
          <p class="item-name">{{item.name}}</p>
          <p class="item-level">{{item.level}} {{item.comment}}</p>
          <p class="item-price">{{item.price}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '1',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg_200x200_32e22bed.jpg',
          level: '3',
          title: '奥林匹克',
          comment: '189',
          price: '110',
          place: '朝阳区'
        },
        {
          id: '2',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
          level: '4',
          title: '野生动物园',
          comment: '100',
          price: '90',
          place: '海淀区'
        },
        {
          id: '3',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1604/78/78873494f26e554090.water.jpg_200x200_331422ad.jpg',
          level: '5',
          title: '京东石林峡',
          comment: '2954',
          price: '58',
          place: '平谷区'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
  .recommend-title
    margin-top: .1rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    text-align:left
  .recommend-item-view
    display: flex
    overflow: hidden
    height: 2.0rem
    background: green
    .recommend-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .recommend-content
      flex: 1
      padding: .1rem
      .item.name
        font-size:.22rem
        line-height: .54rem
</style>
