<!--<template>
  <Carousel :itemsToShow="3.95" :wrapAround="true">
    <Slide v-for="slide in 10" :key="slide">
      <div class="carousel__item">{{ slide }}</div>
    </Slide>

    ...
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Pagination, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';

export default defineComponent({
  name: 'Autoplay',
  components: {
    Carousel,
    Slide,
    Pagination,
  },
});
</script>

<style scoped>
.carousel__slide > .carousel__item {
  transform: scale(1);
  opacity: 0.5;
  transition: 0.5s;
}
.carousel__slide--visible > .carousel__item {
  opacity: 1;
  transform: rotateY(0);
}
.carousel__slide--next > .carousel__item {
  transform: scale(0.9) translate(-10px);
}
.carousel__slide--prev > .carousel__item {
  transform: scale(0.9) translate(10px);
}
.carousel__slide--active > .carousel__item {
  transform: scale(1.1);
}
</style>-->
<template>
  <section class="container container-fluid-md">
    <swiper
        :slides-per-view="1"
        navigation
        :pagination="{ clickable: true }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
    >
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/1.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/2.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/3.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/4.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/5.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/6.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/7.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/1.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/2.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/3.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/4.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/5.png" alt="">
        </div>
        </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
       <div class="image">
          <img src="../assets/image/voice/6.png" alt="">
       </div>
      </swiper-slide>
      <swiper-slide class="slide" style="width:100px !important">
        <div class="image">
          <img src="../assets/image/voice/7.png" alt="">
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>
<script>
  import SwiperCore, { Navigation, Pagination, A11y } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/swiper.min.css";

// install Swiper components
SwiperCore.use([Navigation, Pagination, A11y]);

// Import Swiper styles

  export default {
    components: {
      Swiper,
      SwiperSlide

    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    },
  };
</script>
<style scoped>
div {
  display: inline-block;
}
/*.container {
  overflow-x: hidden;
  max-width: 1140px;
}

.slide {
  margin-right: 100px;
  opacity: 0.2;
}

.image {
  margin-right: 265px;
}

.image img {
  margin-left: 130px;
}

.click {
  opacity: 5;
  width: 145px;
}*/
</style>