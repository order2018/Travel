<template>
  <div class="icons">
      <swiper>
          <swiper-slide v-for="(page,index) in pages" :key="index">
              <div class="icon"
                v-for="item in page"
                :key="item.id"
              >
                  <div class="icon-img">
                      <img class="icon-img-content" :src="item.imgUrl" alt="">
                  </div>
                  <p class="icon-desc">{{item.desc}}</p>
              </div>
          </swiper-slide>
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
        iconList: [
            {
                id:1,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/94/A9/Cii-T1hmH2yIURNDAAAJyfc0kUYAAGMPAP_79EAAAnh702.png',
                desc:'全球WiFi'
            },
            {
                id:2,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G5/M00/BA/9B/Cii-s1rQQK-IRf8xAAAIOKU8KZoAAFjGAP_93sAAAiF451.png',
                desc:'目地参团'
            },
            {
                id:3,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G3/M00/32/38/Cii_Llli3baIed2wAAACgMRu23IAADA0wP__WgAAAKY669.png',
                desc:'婚纱旅拍'
            },
            {
                id:4,
                imgUrl:'https://m3.tuniucdn.com/fb2/t1/G4/M00/2B/43/Cii_J1myMKOIa59DAAAEk3iRAL8AAA1twP_-1UAAASr274.png',
                desc:'主题旅游'
            },
            {
                id:5,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/F3/1C/Cii-T1iULIKIW6kBAAAFJJmHzD4AAG8NwP_-sIAAAU-443.png',
                desc:'蜜月旅游'
            },
            {
                id:6,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/84/64/Cii-U1ir_DyIWjOQAAAMzJwlIzUAAHmAQP_8xsAAAzl573.png',
                desc:'海岛旅游'
            },
            {
                id:7,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/56/7D/Cii9EViFfe2IVXYOAAAJ0Vcji84AAHIGQP_9XMAAAqN711.png',
                desc:'旅游百货'
            },
            {
                id:8,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/97/DA/Cii-TFhvBHiIWtIQAAAD8MUG7VcAAGNiAP_-_QAAAQM018.png',
                desc:'更多'
            },
            {
                id:9,
                imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/94/A9/Cii-T1hmH2yIURNDAAAJyfc0kUYAAGMPAP_79EAAAnh702.png',
                desc:'全球WiFi'
            }
        ]
    }
  },
  computed: {
        pages () {
            const pages = [];
            this.iconList.forEach((item,index) => {
                const page = Math.floor(index / 8);
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            });
            return pages
        }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
    height:0;
    padding-bottom:50%;
.icon
    position:relative;
    overflow:hidden;
    float:left;
    width:25%;
    padding-bottom:25%;
.icon-img
    position:absolute;
    top:0;
    left:0;
    right:0;
    bottomm:.44rem;
    box-sizing:border-box;
    padding:.1rem;
.icon-img-content
    display:block;
    margin:0 auto;
    width:1rem;
    height:100%;
.icon-desc
    position:absolute;
    left:0;
    right:0;
    bottom:0;
    height:.44rem;
    line-height:.44rem;
    color:$darkTextColor;
    text-align:center;
    ellipse()
</style>
