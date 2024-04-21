<template>
  <q-page class="">
    <div class="banner">
      <div class="home">
        <div class="row">
          <div class="col">
            <div class="text-white text-bold text-h3 q-mt-xl q-pt-xl q-pb-lg">
              최고의 실력을 가진 <br />
              외국인 인재를 찾고 계신가요?
            </div>
            <div class="text-white text-h6 q-pb-lg">
              법률 및 인사관리 부담없이 1주일 이내에 원격으로 채용해보세요.
            </div>
            <div class="text-white text-h6 q-pb-lg">개발자가 필요하신가요?</div>

            <div class="flex items-start justify-start gt-sm">
              <q-card flat class="my-card">
                <q-card-section class="text-white">
                  <div class="text-h6">평균 월 120만원</div>
                  <div class="text-subtitle2">
                    임금을 해당 국가를 기준으로 계산합니다.
                  </div>
                </q-card-section>
              </q-card>
              <q-card flat class="my-card">
                <q-card-section class="text-white">
                  <div class="text-h6">최대 3회 인력교체</div>
                  <div class="text-subtitle2">
                    막상 채용해보니 맞지 않아도 걱정하지 마세요.
                  </div>
                </q-card-section>
              </q-card>
              <q-card flat class="my-card" style="width: 40%">
                <q-card-section class="text-white">
                  <div class="text-h6">평균 3일, 최대 10일</div>
                  <div class="text-subtitle2">
                    급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.
                  </div>
                </q-card-section>
              </q-card>
            </div>
          </div>
          <div class="col gt-sm">
            <div class="q-py-xl">
              <CarouselLink />
            </div>
          </div>
        </div>
         <div class="flex items-center justify-center lt-md">
            <div class="q-pa-xl">
              <CarouselLink />
            </div>
          </div>
        <div class="btn-section gt-sm">
          <div class="btn">
            <q-img src="../assets/icon1.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">외 마케팅</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon2.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">퍼블리셔</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon3.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">캐드원(제도사)</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon4.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 세일즈</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon5.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 CS</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon1.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 마케팅</span>
          </div>
        </div>
      </div>
    </div>
    <MyFooter />    
  </q-page>
</template>

<style scoped>
.home {
  max-width: 1170px;
  margin: auto;
}
.banner {
  background-image: url("../assets/banner.png");
  background-repeat: no-repeat;
  background-size: cover;
}
.my-card {
  background-color: transparent !important;
  width: 30%;
  padding-left: 0px;
}
.slide-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.swiper-container {
  position: relative;
  width: 100%;
  height: 400px; /* Adjust height as needed */
}
.swiper-container1 {
  width: 80%;
  height: 60%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  /* Add additional styles for slides */
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.slide-content {
  position: absolute;
  bottom: 20px;
  left: 20px;
  right: 20px;
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}

.swiper-pagination {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
}

.swiper-button-prev,
.swiper-button-next {
  color: #fff;
  font-size: 18px;
  width: 40px;
  height: 40px;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}

.swiper-button-prev {
  left: 10px;
}

.swiper-button-next {
  right: 10px;
}
.btn-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.btn {
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 10px;
  padding: 10px;
  background: #ffffff33;
  border-radius: 10px;
  /* width: 210px; */
}
@media (max-width: 1200px) {
  .banner {
  background-image: url("../assets/banner.png");
  background-repeat: no-repeat;
  /* background-size: cover; */
  height: fit-content;
}
}
</style>

<script>
import { ref } from "vue";
import Swiper from "swiper";
import "swiper/swiper-bundle.css";
import MySlider from "components/MySlider.vue";
import MyFooter from "components/MyFooter.vue";
import CarouselLink from "components/CarouselLink.vue"
import SliderLink from "components/SliderLink.vue"

export default {
  name: "IndexPage",
  components: {
    MyFooter,
    // MySlider,
    CarouselLink,
    // SliderLink,
  },
  mounted() {
    this.swiper = new Swiper(".swiper-container", {
      slidesPerView: 3, // Number of slides to show at once
      centeredSlides: true,
      spaceBetween: 40, // Center the active slide
      loop: true,
      autoplay: {
        delay: 5000,
        disableOnInteraction: false,
      },
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
      // Add more configurations as needed
    });
  },
  beforeUnmount() {
    if (this.swiper) {
      // Destroy swiper
      this.swiper.destroy();
    }
  },
};
</script>
