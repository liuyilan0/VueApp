<template>
  <div>
    <detail-header></detail-header>
    <detail-navigation></detail-navigation>
    <div class="bottom">
      <detail-list :dataList="dataList"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailNavigation from './components/Navigation'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailNavigation,
    DetailList
  },
  data () {
    return {
      dataList: [
        {
          title: '日场票',
          children: [
            {
              title: '奥林匹克塔',
              children: [
                {
                  title: '奥林匹克塔成人票'
                },
                {
                  title: '奥林匹克塔双人票'
                },
                {
                  title: '奥林匹克塔三人票'
                }
              ]
            },
            {
              title: '鸟巢',
              children: [
                {
                  title: '鸟巢成人票'
                }
              ]
            }
          ]
        },
        {
          title: '夜场票',
          children: [
            {
              title: '中国科技馆',
              children: [
                {
                  title: '中国科技馆成人票'
                },
                {
                  title: '中国科技馆双人票'
                },
                {
                  title: '中国科技馆三人票'
                }
              ]
            },
            {
              title: '八达岭长城',
              children: [
                {
                  title: '八达岭长城儿童票'
                },
                {
                  title: '八达岭长城成人票'
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
  .bottom
    height: 50rem
</style>
