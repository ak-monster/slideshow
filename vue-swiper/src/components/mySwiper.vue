<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide><img src="../img/1.jpeg" alt=""></swiper-slide>
    <swiper-slide><img src="../img/2.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="../img/3.png" alt=""></swiper-slide>
    <swiper-slide><img src="../img/4.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="../img/5.jpg" alt=""></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    <div class="swiper-button-prev"></div><!--左箭头。如果放置在swiper-container外面，需要自定义样式。-->
    <div class="swiper-button-next"></div><!--右箭头。如果放置在swiper-container外面，需要自定义样式。-->
  </swiper>
</template>

<script>
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'
export default {
  name: 'HelloWorld',
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swiperOptions: {
        speed: 600,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        loop: true,
        autoplay: {
          delay: 2000,
          disableOnInteraction: false
        },
        effect: 'coverflow'
      }
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .swiper-container {
    width: 600px;
    height: 338px;
  }

  img {
    width: 100%;
    height: 100%;
  }
</style>
