<template>
  <section class="container container-fluid-md">
    <swiper
        :slides-per-view="1"
        navigation
        :pagination="{ clickable: true }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
    >
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/1.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/2.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/3.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/4.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/5.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/6.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/7.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/1.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/2.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/3.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/4.png" alt="">
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="image">
          <img src="../assets/image/voice/5.png" alt="">
        </div>
        </swiper-slide>
      <swiper-slide class="slide">
       <div class="image">
          <img src="../assets/image/voice/6.png" alt="">
       </div>
      </swiper-slide>
      <swiper-slide class="slide">
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