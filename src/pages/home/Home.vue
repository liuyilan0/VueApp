<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :imgList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommend :recommendList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeData () {
      axios.get('/api/home.json')
        .then(this.getHomeDataSuccess)
    },
    getHomeDataSuccess (res) {
      if (res.data.code === '200' && res.data.data) {
        const response = res.data.data
        this.city = response.city
        this.swiperList = response.swiperList
        this.iconList = response.iconList
        this.recommendList = response.recommendList
        this.weekendList = response.weekendList
      }
    }
  },
  mounted () {
    this.getHomeData()
  }
}
</script>

<style scoped>

</style>
