<template>
  <div class="slider-image">
    <swiper-container
      class="swiper-container"
      direction="vertical"
      :mousewheel="true"
      @swiperslidechange="handleSwiperChange"
    >
      <swiper-slide class="swiper-slide">
        <img :src="image1" class="swiper-image" />
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image5" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__fadeInUp: activeIndex === 1 }"
          style="top: 484px; left: 65px; text-align: center; line-height: 1.1"
        >
          <div class="title">年度关键词</div>
          <div class="content">
            <span class="big blue">AI </span>
            <span class="big blue">职业 </span>
            <span class="big blue">健康</span>
          </div>
          <div class="content">写了 <span class="big blue">3.2万</span> 行代码</div>
          <div class="content">体重增加了 <span class="big blue">1.1</span> KG</div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image2" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__slideInLeft: activeIndex === 2 }"
          style="top: 186px; left: 32px; line-height: 1.2"
        >
          <div class="title">今年</div>
          <div class="content">发布了 <span class="big yellow">92</span> 个视频</div>
          <div class="content">收获了 <span class="big yellow">672万</span> 播放量</div>
          <div class="content">共 <span class="big yellow">13万</span> 个互动量</div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image4" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__fadeInUp: activeIndex === 3 }"
          style="top: 218px; left: 32px; text-align: left; line-height: 1.1"
        >
          <div class="title">今年</div>
          <div class="content">看了 <span class="big green">1</span> 本书</div>
          <div class="content">短视频倒是看了 <span class="big green">2.7万</span> 个</div>
          <div class="content">
            明年要多做&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;优质视频哦<span class="big green"
              >！</span
            >
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image3" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__slideInRight: activeIndex === 4 }"
          style="top: 20px; right: 32px; text-align: right"
        >
          <div class="title">今年的第一次</div>
          <div class="small-content"><span class="pink">第一次</span>收获点赞过万的视频</div>
          <div class="small-content"><span class="pink">第一次</span>召集大家做海外的代码项目</div>
          <div class="small-content"><span class="pink">第一次</span>独自开车上高速</div>
          <div class="small-content">
            <span class="pink">第一次</span>遇到工作中最大的挑战<br />并战胜了它
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image6" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__fadeInDown: activeIndex === 5 }"
          style="top: 20px; left: 32px; text-align: left"
        >
          <div class="title">干饭时间</div>
          <div class="small-content">今年早饭只吃了<span class="big1 pink">84</span>次</div>
          <div class="small-content">最早的早饭是<span class="big1 pink">06:18</span></div>
          <div class="small-content">最晚的晚饭是<span class="big1 pink">23:37</span></div>
          <div class="small-content">爸妈不在身边，</div>
          <div class="small-content">也要记得好好吃饭！</div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image7" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__fadeInUp: activeIndex === 6 }"
          style="top: 464px; right: 32px; line-height: 1.1; text-align: right"
        >
          <div class="title">今年</div>
          <div class="content">运动了 <span class="big yellow">18</span> 天</div>
          <div class="content">消耗了 <span class="big yellow">3780</span> 大卡</div>
          <div class="content">超越了 <span class="big yellow">29%</span> 的人</div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <img :src="image8" class="swiper-image" />
        <div
          class="text-wrapper animate__animated"
          :class="{ animate__zoomIn: activeIndex === 7 }"
          style="top: 20px; left: 32px; text-align: left"
        >
          <div class="content">2025，辛苦了</div>
          <div class="content">2026，请优先爱自己</div>
          <div
            class="content"
            style="line-height: 1; position: absolute; top: 241px; right: -72px; text-align: right"
          >
            <div>健康是 <span class="big yellow">1</span></div>
            <div>其余是后面的 <span class="big yellow">0</span></div>
          </div>
          <div
            class="content"
            style="line-height: 1; position: absolute; top: 600px; left: 40px; width: 100%"
          >
            珍惜此刻，即是未来
          </div>
        </div>
      </swiper-slide>
    </swiper-container>
  </div>
</template>

<script setup>
import image1 from '@/assets/images/1.jpg'
import image2 from '@/assets/images/2.jpg'
import image3 from '@/assets/images/3.jpg'
import image4 from '@/assets/images/4.jpg'
import image5 from '@/assets/images/5-1.png'
import image6 from '@/assets/images/6.jpg'
import image7 from '@/assets/images/7.jpg'
import image8 from '@/assets/images/8.jpg'
import { ref } from 'vue'

const activeIndex = ref(0)
const handleSwiperChange = (e) => {
  const [item] = e.detail
  activeIndex.value = item.realIndex
}
</script>

<style lang="scss" scoped>
.slider-image {
  margin: 0 auto;
  max-width: 414px;
  width: 100vw;
  height: 100dvh;
  font-family: 'jing-nan-bo-bo-hei';
  .swiper-container {
    width: 100%;
    height: 100%;
    .swiper-slide {
      position: relative;
      width: 100%;
      height: 100%;
      overflow: hidden;
      .text-wrapper {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 1;
        font-size: 32px;
        color: #000;
      }
      .title {
        font-size: 48px;
        font-weight: bold;
      }
      .content {
        font-size: 32px;
        letter-spacing: -3px;
      }
      .small-content {
        font-size: 24px;
        letter-spacing: 0;
      }
      .green {
        color: #00d048;
        font-weight: bold;
      }
      .pink {
        color: #ff6699;
        font-weight: bold;
      }
      .yellow {
        color: #ffa800;
        font-weight: bold;
      }
      .blue {
        color: #00c1ff;
        font-weight: bold;
      }
      .big1 {
        font-size: 32px;
        font-weight: bold;
      }
      .big {
        font-size: 48px;
        font-weight: bold;
      }
      .swiper-image {
        width: 100%;
        height: 100%;
        transform: scale(1.01);
        object-fit: cover;
      }
    }
  }
}
</style>
