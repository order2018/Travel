<template>
  <div class="recommend">
      <div class="title">热销推荐</div>
      <ul>
          <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
              <div class="item-img-wrapper">
                  <img class="item-img" :src="item.imgUrl" alt="">
              </div>
              <div class="item-info">
                  <p class="item-title">{{item.title}}</p>
                  <p class="item-desc">{{item.desc}}</p>
                  <button class="item-button">查看详情</button>
              </div>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
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
            },
            {
                id:4,
                title:'日本东京-富士山-京都',
                imgUrl:'https://m.tuniucdn.com/filebroker/cdn/snc/80/e5/80e54f355e0f366f0d1c4e817d5a3652_w180_h180_c1_t0.jpg',
                desc:'日本东京-富士山-京都-大阪6或7日游&gt;孝爸妈 ABE全程含餐无忧 无虑 保证一晚舒适温泉 一万二日币高规餐标 升级一晚高品质住宿 CD线6天4晚 经典囊括'
            },
            {
                id:5,
                title:'毛泽东故居1日游',
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/F7/D9/Cii-TlgjEquIRrVfADDqJK-L9bwAAESfQDKwskAMOo8631_w640_h320_c1_t0.jpg',
                desc:'长沙-韶山-橘子洲-滴水洞-毛泽东故居1日游>（早班）跟着主席诗词去旅行 长沙韶山一天游遍 走专用通道 含主席像章 手绘明信片 矿泉水'
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
.item
    overflow:hidden;
    display:flex;
    height:1.9rem;
.item-img
    width:1.7rem;
    height:1.7rem;
    padding:.1rem;
.item-info
    flex:1
    padding:.1rem;
    min-width:0;
.item-title
    line-height:.54rem;
    font-size:.32rem;
    ellipse();
.item-desc
    line-height:.4rem;
    color:#ccc;
    ellipse();
.item-button
    line-height:.44rem;
    margin-top:.16rem;
    background:#ff9300;
    padding:0 .2rem;
    border-radius:.06rem;
    color:#fff;
</style>
