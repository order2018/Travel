<template>
  <div class="home">
      <home-header></home-header>
      <home-swipe></home-swipe>
      <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header';
import HomeSwipe from './components/Swipe';
import HomeIcons from './components/Icons';
export default {
  name: 'Home',
  data () {
    return {

    }
  },
  components: {
      HomeHeader,
      HomeSwipe,
      HomeIcons
  }
}
</script>

<style scoped>

</style>
