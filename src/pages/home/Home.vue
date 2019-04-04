<template>
  <div class="home">
      <home-header :city="city"></home-header>
      <home-swipe :list="swiperList"></home-swipe>
      <home-icons :list="iconList"></home-icons>
      <home-recommend :list="recommendList"></home-recommend>
      <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header';
import HomeSwipe from './components/Swipe';
import HomeIcons from './components/Icons';
import HomeRecommend from './components/Recommend';
import HomeWeekend from './components/Weekend';
import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
        city:'',
        swiperList:[],
        iconList:[],
        recommendList:[],
        weekendList:[]
    }
  },
  components: {
      HomeHeader,
      HomeSwipe,
      HomeIcons,
      HomeRecommend,
      HomeWeekend
  },
  methods: {
    getHomeInfo () {
        axios.get('/api/index.json')
          .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
        res = res.data;
        if (res.ret && res.data) {
            const data = res.data
            this.city = data.city
            this.swiperList = data.swiperList
            this.iconList = data.iconList
            this.recommendList = data.recommendList
            this.weekendList = data.weekendList
        }
    }
  },
  mounted() {
      this.getHomeInfo()
  }
}
</script>

<style scoped>

</style>
