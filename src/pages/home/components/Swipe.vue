<template>
  <div class="swipe">
      <swiper :options="swiperOption">
          <swiper-slide v-for="(slide, index) in swiperList" :key="slide.id">
              <img class="swipe-img" :src="slide.imgUrl" alt="">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwipe',
  data () {
    return {
        swiperOption: {
            pagination: '.swiper-pagination',
            loop:true,
            Autoplay:{
                delay: 3000,
            }
        },
        swiperList: [
            {
                id:1,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/F8/42/Cii9EFbCm_OIVVgEABSzZOOmRIcAAB4OQHOoksAFLN8825_w450_h300_c1_t0_w640_h480_c1_t0_w640_h320_c1_t0.jpg'
            },
            {
                id:2,
                imgUrl:'https://m.tuniucdn.com/filebroker/cdn/prd/63/de/63de210ccc692ce73149f42a42080aec_w640_h480_c1_t0_w640_h320_c1_t0.jpg'
            },
            {
                id:3,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G5/M00/03/BE/Cii-slyi_76IY1PrAB-vV5-IFfEAAUztgElPkIAH69v447_w640_h480_c1_t0_w640_h320_c1_t0.jpg'
            }
        ]
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
        padding-bottom:48.25%;
        background-color:#eee;
    .swipe-img
        width:100%;
</style>
