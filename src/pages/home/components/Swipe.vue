<template>
  <div class="swipe">
      <swiper :options="swiperOption" v-if="showSwiper">
          <swiper-slide v-for="(slide, index) in list" :key="slide.id">
              <img class="swipe-img" :src="slide.imgUrl" alt="">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwipe',
  props: {
    list: Array
  },
  data () {
    return {
        swiperOption: {
            pagination: '.swiper-pagination',
            loop:true,
            Autoplay:{
                delay: 3000,
            }
        }
    }
  },
  computed: {
    showSwiper () {
        return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
    .swipe>>>.swiper-pagination-bullet-active
     background:#fff;
    .swipe
        overflow hidden
        width:100%;
        height:0;
        padding-bottom:31.25%;
        background-color:#eee;
    .swipe-img
        width:100%;
</style>
