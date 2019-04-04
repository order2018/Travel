<template>
  <div class="home">
      <home-header></home-header>
      <home-swipe></home-swipe>
      <home-icons></home-icons>
      <home-recommend></home-recommend>
  </div>
</template>

<script>
import HomeHeader from './components/Header';
import HomeSwipe from './components/Swipe';
import HomeIcons from './components/Icons';
import HomeRecommend from './components/Recommend';
export default {
  name: 'Home',
  data () {
    return {

    }
  },
  components: {
      HomeHeader,
      HomeSwipe,
      HomeIcons,
      HomeRecommend
  }
}
</script>

<style scoped>

</style>
