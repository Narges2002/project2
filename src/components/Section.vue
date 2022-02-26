<template>
    <section class="section container container-fluid-md">   
         <div class="section-header">
            <h2>چرا رژیم دکتر کرمانی؟</h2>
        </div>
        <div class="diet-Property p-0">
            <div class="swiper-carousel swiper-theme swiper-slider-diet-Property swiper-rtl swiper-loaded swiper-drag">
                <swiper
                :slides-per-view="1"
                navigation
                :pagination="{ clickable: true }"
                @swiper="onSwiper"
                @slideChange="onSlideChange"
                class="swiper-stage swiper-stage-outer">
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px;">
                        <div class="item item-01">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/11.png">
                            </div>
                            <h3 class="text-primary diet-Property-title">ویزیت رایگان</h3>
                            <div class="diet-Property-text">
                                <p>
                                    در هر دوره&zwnj;ی سه ماهه رژیم دکتر کرمانی هر زمان که نیاز به کمک داشتید، می&zwnj;تونید از خدمات رایگان مشاوره و ویزیت کارشناس&zwnj;های تغذیه ما برای رفع مشکلتون استفاده کنید. کافیه اعلام نیاز کنید تا با شما تماس بگیریم.
                                </p>
                            </div>
                            <svg class="svg-01" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint3_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint3_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5"   gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#7367F0"></stop>
                                        <stop offset="1" stop-color="#CE9FFC"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important;">
                        <div class="item item-02">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/22.png">
                            </div>
                            <h3 class="diet-Property-title">نتایج و امار مثبت</h3>
                            <div class="diet-Property-text">
                                <p>ما در مجموعه دکترکرمانی بیش از 25 سال در حوزه سلامتی فعالیت داریم و تونستیم حدود یک میلیون نفر رو با این رژیم به وزن دلخواهشون برسونیم.
                                </p>
                            </div>
                            <svg class="svg-02" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint0_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint0_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#FD6585"></stop>
                                        <stop offset="1" stop-color="#FFD3A5"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important;">
                        <div class="item item-03">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/33.png">
                            </div>
                            <h3 class="diet-Property-title">پشتیبانی</h3>
                            <div class="diet-Property-text">
                                <p>ما به صورت ۱۲ ساعته آماده&zwnj;ی پاسخگویی به شما عزیزان هستیم. هر وقت به کمک نیاز داشتین می&zwnj;تونید به صورت تلفنی یا آنلاین باهامون در ارتباط باشید.
                                <br>
                                علاوه بر پاسخگویی به سوالات شما، روند کاهش وزنتون رو هم بررسی می&zwnj;کنیم.
                                </p>
                            </div>
                            <svg class="svg-03" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint1_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint1_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#28C76F"></stop>
                                        <stop offset="1" stop-color="#81FBB8"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important;">
                        <div class="item item-04">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/44.png">
                            </div>
                            <h3 class="diet-Property-title">تنوع لیست غذایی</h3>
                            <div class="diet-Property-text">
                                <p>با رژیم دکتر کرمانی هیچ محدودیت غذایی نداری و هر غذایی که فکرشو کنی در برنامه غذایی تون هست و میتونید به دلخواه خودتون انتخاب کنید و در کنار سفره خانواده رژیم بگیرید.
                                </p>
                            </div>
                            <svg class="svg-04" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint2_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint2_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#F072B6"></stop>
                                        <stop offset="1" stop-color="#FFF886"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important;">
                        <div class="item item-01">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/11.png">
                            </div>
                            <h3 class="text-primary diet-Property-title">ویزیت رایگان</h3>
                            <div class="diet-Property-text">
                                <p>
                                    در هر دوره&zwnj;ی سه ماهه رژیم دکتر کرمانی هر زمان که نیاز به کمک داشتید، می&zwnj;تونید از خدمات رایگان مشاوره و ویزیت کارشناس&zwnj;های تغذیه ما برای رفع مشکلتون استفاده کنید. کافیه اعلام نیاز کنید تا با شما تماس بگیریم.
                                </p>
                            </div>
                            <svg class="svg-01" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint3_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint3_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5"   gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#7367F0"></stop>
                                        <stop offset="1" stop-color="#CE9FFC"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important">
                        <div class="item item-02">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/22.png">
                            </div>
                            <h3 class="diet-Property-title">نتایج و امار مثبت</h3>
                            <div class="diet-Property-text">
                                <p>
                                    ما در مجموعه دکترکرمانی بیش از 25 سال در حوزه سلامتی فعالیت داریم و تونستیم حدود یک میلیون نفر رو با این رژیم به وزن دلخواهشون برسونیم.
                                </p>
                            </div>
                            <svg class="svg-02" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint0_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint0_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#FD6585"></stop>
                                        <stop offset="1" stop-color="#FFD3A5"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important">
                        <div class="item item-03">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/33.png">
                            </div>
                            <h3 class="diet-Property-title">پشتیبانی</h3>
                            <div class="diet-Property-text">
                                <p>ما به صورت ۱۲ ساعته آماده&zwnj;ی پاسخگویی به شما عزیزان هستیم. هر وقت به کمک نیاز داشتین می&zwnj;تونید به صورت تلفنی یا آنلاین باهامون در ارتباط باشید.
                                <br>
                                علاوه بر پاسخگویی به سوالات شما، روند کاهش وزنتون رو هم بررسی می&zwnj;کنیم.
                                </p>
                            </div>
                            <svg class="svg-03" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint1_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint1_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#28C76F"></stop>
                                        <stop offset="1" stop-color="#81FBB8"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                    <swiper-slide class="swiper-item" style="width: 270px; margin-left: 10px; hight: 87% !important">
                        <div class="item item-04">
                            <div class="diet-Property-img">
                                <img src="../assets/image/diet-Property/44.png">
                            </div>
                            <h3 class="diet-Property-title">تنوع لیست غذایی</h3>
                            <div class="diet-Property-text">
                                <p>با رژیم دکتر کرمانی هیچ محدودیت غذایی نداری و هر غذایی که فکرشو کنی در برنامه غذایی تون هست و میتونید به دلخواه خودتون انتخاب کنید و در کنار سفره خانواده رژیم بگیرید.
                                </p>
                            </div>
                            <svg class="svg-04" width="270" height="92" viewBox="0 0 270 92" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M270 0H118.5C73.7 39.2 20.8333 56.3333 0 60V90.5C160.4 99.3 246.833 33.8333 270 0Z" fill="url(#paint2_linear)" fill-opacity="1">
                                </path>
                                <defs>
                                    <linearGradient id="paint2_linear" x1="-0.499999" y1="98.5" x2="206.5" y2="-14.5" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#F072B6"></stop>
                                        <stop offset="1" stop-color="#FFF886"></stop>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                    </swiper-slide>
                </swiper>
            </div>
        </div>
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
.container {
    max-width: 1140px;
}
*::before, *::after {
    box-sizing: border-box;
}
.section-header {
    color: #b1346e;
    position: relative;
    padding: 40px 0 20px;
    margin: 0 !important;
}
.section-header h2 {
    padding-right: 40px;
    font-size: 20px;
    font-weight: 600px;
}
.section-header h2::before {
    content: "";
    position: absolute;
    top: 58%;
    right: 0;
    background-color: #b1346e;
    width: 30px;
    height: 2px;
}
.swiper-carousel {
    display: none;
    z-index: 1;
}
.swiper-carousel .swiper-item {
    position: relative;
    min-height: 1px;
    float: left;
}
.swiper-slider-diet-Property .item-04 .diet-Property-title {
    color: #f074b5;
}
.swiper-slider-diet-Property .item-04 .svg-04 {
    position: absolute;
    top: 0;
    left: 0;
}
.swiper-slider-diet-Property .item svg {
    opacity: 0.12;
}
svg {
    overflow: hidden;
    vertical-align: middle;
}
.swiper-carousel.swiper-rtl {
    direction: rtl;
}
.swiper-carousel.swiper-loaded {
    display: block;
}
.swiper-carousel .swiper-stage-outer {
    position: relative;
    overflow-x: hidden;
}
.swiper-slider-diet-Property .swiper-stage {
    display: -webkit-box;
    display: flex;
    position: relative;
    touch-action: manipulation;
}
element.style {
    width: 270px !important;
    margin-left: 10px;
}
.swiper-carousel.owl-rtl .swiper-item {
    float: right;
}
.swiper-slider-diet-Property .item-04 {
    position: relative;
}
.swiper-slider-diet-Property .item {
    background-color: white;
    border-radius: 15px;
    border: #e5e8ef solid 1px;
    padding: 30px 15px 0;
    height: 100% !important;
}
.diet-Property-img {
    border-radius: 15px;
    width: 90px !important;
    height: 90px !important;
    display: -webkit-box;
    display: flex;
}
.item-01 .svg-01 {
    position: absolute;
    top: 0;
    left: 0;
}
.item-02 .svg-02 {
    position: absolute;
    top: 0;
    left: 0;
}
.item-03 .svg-03 {
    position: absolute;
    top: 0;
    left: 0;
}
.diet-Property-title {
    padding: 30px 0 5px;
    font-size: 18px;
    font-weight: 600;
    text-align: justify;
}
.diet-Property-text {
    text-align: justify;
    color: #434343;
    font-size: 14px;
}
p {
    margin-top: 0;
    margin-bottom: 1rem;
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
}
.swiper-slider-diet-Property .item-03 .diet-Property-title {
    color: #2bc971;
}
.swiper-slider-diet-Property .item-02 .diet-Property-title {
    color: #fd6786;
}
</style>