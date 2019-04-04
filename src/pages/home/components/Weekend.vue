<template>
  <div class="weekend">
      <div class="title">周末去哪儿</div>
      <ul>
          <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
              <div class="item-img-wrapper">
                  <img class="item-img" :src="item.imgUrl" alt="">
              </div>
              <div class="item-info">
                  <p class="item-title">{{item.title}}</p>
                  <p class="item-desc">{{item.desc}}</p>
              </div>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
        recommendList:[
            {
                id:1,
                title:'大连圣亚海洋世界',
                imgUrl:'https://m.tuniucdn.com/filebroker/cdn/olb/03/96/039602ad61f2df205f3bb7ea024dbc5a_w350_h0_c0_t0.jpg',
                desc:'烂漫大连首站，浪漫的海洋主题乐园'
            },
            {
                id:2,
                title:'中央格兰德岛',
                imgUrl:'https://m.tuniucdn.com/filebroker/cdn/snc/6b/de/6bdefd097fd57d65e6349420befc81eb_w350_h0_c0_t0.jpg',
                desc:'马尔代夫伊露岛Irufushi4晚6日自由行>两位儿童优惠，免费水飞，儿童设施齐全，亲子游首选，中文服务，四晚岛上，途牛自营'
            },
            {
                id:3,
                title:'西藏林芝-拉萨-布达拉宫',
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G3/M00/68/CA/Cii_LlmAE7qIfn2RAAOHtz7m_LYAAF4ewJGEnMAA4fP253_w180_h180_c1_t0.jpg',
                desc:'西藏林芝-拉萨-布达拉宫-羊湖飞卧10日游>回北京，缓解高反首选0购0自，林进拉出低海拔入藏，途牛自营地接&全程高档住宿，邂逅桃源+南迦巴瓦峰'
            }
        ]
    }
  },
  computed: {

  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
    margin-top:.2rem;
    line-height:.8rem;
    background:#eee;
    text-indent:.2rem;
.item-img-wrapper
    overflow:hidden;
    height:0;
    padding-bottom:33.9%;
.item-img
    width:100%;
.item-info
    padding:.1rem;
.item-title
    line-height:.54rem;
    font-size:.32rem;
    ellipse();
.item-desc
    line-height:.4rem;
    color:#ccc;
    ellipse();
</style>
