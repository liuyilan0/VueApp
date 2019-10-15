<template>
  <div>
    <detail-header :bannerImgUrl="bannerImgUrl" :bannerList="bannerList"></detail-header>
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
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailNavigation,
    DetailList
  },
  data () {
    return {
      bannerImgUrl: '',
      bannerList: [],
      dataList: []
    }
  },
  mounted () {
    this.getDetailInfo()
  },
  methods: {
    getDetailInfo () {
      axios.get('/api/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.getDetailInfoSuccess)
    },
    getDetailInfoSuccess (res) {
      res = res.data
      if (res && res.data) {
        const response = res.data
        this.bannerImgUrl = response.bannerImgUrl
        this.bannerList = response.bannerList
        this.dataList = response.dataList
      }
    }
  }
}
</script>

<style lang='stylus' scoped>
  .bottom
    height: 50rem
</style>
