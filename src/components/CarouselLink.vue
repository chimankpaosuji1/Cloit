<template>
  <q-swiper class="swiper mySwiper">
    <div class="swiper-wrapper">

      <div class="card swiper-slide">
        <div class="card__image">
          <q-img src="../assets/profile.svg" alt="card image" />
        </div>

        <div class="card__content">
          <span class="card__title">Abhishek Gupta</span>
          <span class="card__name">마케팅 · 2y+</span>
          <div  class="q-mt-sm flex flex-col items-center justify-center  q-gutter-md">
            <q-btn outline  label="마케팅 콘텐츠 제작" color="black" class="brief"/>
            <q-btn outline  label="인스타그램 관리" color="black"  class="brief"/>
            <div class="flex items-center justify-between q-mt-sm">
              <q-btn outline push color="black" label="블로그 글 작성" class="brief"/>
              <q-btn outline  label="트위터 관리" color="black" class="brief"/>
            </div>
          </div>
        </div>
      </div>

      <div class="card swiper-slide">
        <div class="card__image">
          <q-img src="../assets/profile.svg" alt="card image" />
        </div>

        <div class="card__content">
          <span class="card__title">Abhishek Gupta</span>
          <span class="card__name">마케팅 · 2y+</span>
          <div  class="q-mt-sm flex flex-col items-center justify-center  q-gutter-md">
            <q-btn outline  label="마케팅 콘텐츠 제작" color="black" class="brief"/>
            <q-btn outline  label="인스타그램 관리" color="black"  class="brief"/>
            <div class="flex items-center justify-between q-mt-sm">
              <q-btn outline push color="black" label="블로그 글 작성" class="brief"/>
              <q-btn outline  label="트위터 관리" color="black" class="brief"/>
            </div>
          </div>
        </div>
      </div>
      <div class="card swiper-slide">
        <div class="card__image">
          <q-img src="../assets/profile.svg" alt="card image" />
        </div>

        <div class="card__content">
          <span class="card__title">Abhishek Gupta</span>
          <span class="card__name">마케팅 · 2y+</span>
          <div  class="q-mt-sm flex flex-col items-center justify-center  q-gutter-md">
            <q-btn outline  label="마케팅 콘텐츠 제작" color="black" class="brief"/>
            <q-btn outline  label="인스타그램 관리" color="black"  class="brief"/>
            <div class="flex items-center justify-between q-mt-sm">
              <q-btn outline push color="black" label="블로그 글 작성" class="brief"/>
              <q-btn outline  label="트위터 관리" color="black" class="brief"/>
            </div>
          </div>
        </div>
      </div>
         
      
    </div>
  </q-swiper>
</template>

<script>
import Swiper from "swiper";
import "swiper/swiper-bundle.css";

import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/pagination";
import "swiper/css/navigation";

export default {
  name: "CarouselLink",
  mounted() {
    this.swiper = new Swiper(".mySwiper", {
      slidesPerView: "auto", // Number of slides to show at once
      centeredSlides: true, // Center the active slide
      loop: true,
      effect: "coverflow",
      grabCursor: true,
      coverflowEffect: {
        rotate: 0,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: false,
      },
    
     
     

      // Add more configurations as needed
    });
  },
  beforeUnmount() {
    if (this.swiper) {
      this.swiper.destroy();
    }
  },
};
</script>

<style>
.swiper {
  width: 100%;
}

.swiper-wrapper {
  width: 100%;
  height: 35em;
  display: flex;
  align-items: center;
}

.card {
  width: 40%;
  height: 90%;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 0 2em rgba(0, 0, 0, 0.2);
  padding: 2rem;

  display: flex;
  align-items: center;
  flex-direction: column;

  margin: 0 2em;
}

.swiper-slide:not(.swiper-slide-active) {
 background: #EDFCFF;
  width: 40%;
  height: 80%;
  margin-left: -200px;
  z-index: -1;
  margin-right: -200px;
}

.card__image {
  width: 10em;
  height: 10em;
  border-radius: 50%;
  border: 5px solid var(--color);
  padding: 3px;
  margin-bottom: 2em;
}

.card__image img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
}

.card__content {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.card__title {
  font-size: 24px;
  font-weight: 900;
  position: relative;
  top: 0.2em;
}

.card__name {
  font-size: 16px;
  font-weight: 900;
}

.card__text {
  text-align: center;
  font-size: 1.1rem;
  margin: 1em 0;
}

.card__btn {
  background-color: var(--color);
  color: #fff;
  font-size: 1rem;
  text-transform: uppercase;
  font-weight: 600;
  border: none;
  padding: 0.5em;
  border-radius: 0.5em;
  margin-top: 0.5em;
  cursor: pointer;
}
.breif {
  font-size: 16px;
}
@media (max-width: 1200px) {
  .brief {
  font-size: 12px;
}
.card {
  width: 60%;
  
}
}
</style>
