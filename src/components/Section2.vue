<template>
  <div id="Section2">
      <div class="Header">
            <h2>نتایج موفق دوره های قبل</h2>
      </div>
      <div class="slider">
        <swiper
        class="swiper"
        :slides-per-view="1"
        navigation
        :pagination="{ clickable: true }"
        :autoplay='{"delay": 2500,"disableOnInteraction": false}'
        @swiper="onSwiper"
        @slideChange="onSlideChange"
        >
              <swiper-slide>
                  <img src="../assets/images/Slider/01.jpg">
              </swiper-slide>
              <swiper-slide>
                  <img src="../assets/images/Slider/02.jpg">
                  </swiper-slide>
              <swiper-slide>
                  <img src="../assets/images/Slider/03.jpg">
              </swiper-slide>
              <swiper-slide>
                  <img src="../assets/images/Slider/04.jpg">
              </swiper-slide>
              <swiper-slide>
                  <img src="../assets/images/Slider/05.jpg">
              </swiper-slide>
        </swiper>
      </div>
  </div>
</template>
<script>
import SwiperCore, { Navigation, Pagination, Autoplay} from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/swiper.min.css";
import "swiper/components/pagination/pagination.min.css";
import "swiper/esm/components/autoplay/autoplay.js";

// install Swiper components
SwiperCore.use([Navigation, Pagination,Autoplay]);

// Import Swiper styles
  export default {
    components: {
      Swiper,
      SwiperSlide,
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
#Section2 {
    text-align: center;
    margin-bottom: 30px;
}
img {
  width: 100%;
}
.Header h2 {
    font-size: 21px;
    position: relative;
}
.Header ::before {
    content: "";
    position: absolute;
    bottom: 27%;
    right: 0;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 17%;
    height: 2px;
}
.Header ::after {
    content: "";
    position: absolute;
    bottom: 27%;
    left: 0;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 17%;
    height: 2px;
}
</style>