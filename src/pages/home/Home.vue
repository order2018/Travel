<template>
  <div class="home">
      <home-header></home-header>
      <home-swipe></home-swipe>
  </div>
</template>

<script>
import HomeHeader from './components/Header';
import HomeSwipe from './components/Swipe';
export default {
  name: 'Home',
  data () {
    return {

    }
  },
  components: {
      HomeHeader,
      HomeSwipe
  }
}
</script>

<style scoped>

</style>
