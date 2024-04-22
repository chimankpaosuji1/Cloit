<template>
  <section class="section">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide card">
          <div class="card__image">
            <q-img src="../assets/profile.svg" alt="card image" />
          </div>

          <div class="card__content">
            <span class="card__title">Abhishek Gupta</span>
            <span class="card__name">마케팅 · 2y+</span>
            <div
              class="q-mt-sm flex flex-col items-center justify-center q-gutter-md"
            >
              <q-btn
                outline
                label="마케팅 콘텐츠 제작"
                color="black"
                class="brief"
              />
              <q-btn
                outline
                label="인스타그램 관리"
                color="black"
                class="brief"
              />
              <div class="flex items-center justify-between q-mt-sm">
                <q-btn
                  outline
                  push
                  color="black"
                  label="블로그 글 작성"
                  class="brief"
                />
                <q-btn
                  outline
                  label="트위터 관리"
                  color="black"
                  class="brief"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="swiper-slide card">
          <div class="card__image">
            <q-img src="../assets/profile.svg" alt="card image" />
          </div>

          <div class="card__content">
            <span class="card__title">Abhishek Gupta</span>
            <span class="card__name">마케팅 · 2y+</span>
            <div
              class="q-mt-sm flex flex-col items-center justify-center q-gutter-md"
            >
              <q-btn
                outline
                label="마케팅 콘텐츠 제작"
                color="black"
                class="brief"
              />
              <q-btn
                outline
                label="인스타그램 관리"
                color="black"
                class="brief"
              />
              <div class="flex items-center justify-between q-mt-sm">
                <q-btn
                  outline
                  push
                  color="black"
                  label="블로그 글 작성"
                  class="brief"
                />
                <q-btn
                  outline
                  label="트위터 관리"
                  color="black"
                  class="brief"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="swiper-slide card">
          <div class="card__image">
            <q-img src="../assets/profile.svg" alt="card image" />
          </div>

          <div class="card__content">
            <span class="card__title">Abhishek Gupta</span>
            <span class="card__name">마케팅 · 2y+</span>
            <div
              class="q-mt-sm flex flex-col items-center justify-center q-gutter-md"
            >
              <q-btn
                outline
                label="마케팅 콘텐츠 제작"
                color="black"
                class="brief"
              />
              <q-btn
                outline
                label="인스타그램 관리"
                color="black"
                class="brief"
              />
              <div class="flex items-center justify-between q-mt-sm">
                <q-btn
                  outline
                  push
                  color="black"
                  label="블로그 글 작성"
                  class="brief"
                />
                <q-btn
                  outline
                  label="트위터 관리"
                  color="black"
                  class="brief"
                />
              </div>
            </div>
          </div>
        </div>        
      </div>
      <!-- Add Pagination -->
      <div class="swiper-pagination"></div>
    </div>
  </section>
</template>

<script>
import Swiper from "swiper";
import "swiper/swiper-bundle.css";

export default {
  name: "SliderLink",
  mounted() {
    this.swiper = new Swiper(".swiper", {
      effect: "coverflow",
      grabCursor: true,
      centeredSlides: true,
      slidesPerView: "auto",
      coverflowEffect: {
        rotate: 0,
        stretch: 0,
        depth: 100,
        modifier: 2,
        slideShadows: true,
      },
      loop: true,
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
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
.section {
  position: relative;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

  overflow: hidden;
}

.section .swiper {
  width: 100%;
  padding-top: 50px;
  padding-bottom: 50px;
}


.section .swiper-slide {
  width: 300px;
  height: 400px;
  box-shadow: 0 15px 50px rgba(0, 0, 0, 0.2);
  filter: blur(1px);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: end;
  align-items: self-start;
}
.section .swiper-slide:not(.swiper-slide-active) {
  filter: blur(2px);
  background: #edfcff;
  height: 390px;
  margin-top: 10px;
  z-index: -10px;
}
.section .swiper-slide-active {
  filter: blur(0px);
}

.section .swiper-pagination-bullet,
.section .swiper-pagination-bullet-active {
  background: #fff;
}

.section .swiper-slide span {
  color: #000;
  display: inline-block;
  border-radius: 0 20px 20px 0px;
  font-family: "poppins", sans-serif;
}

.section .swiper-3d .swiper-slide-shadow-left,
.section .swiper-3d .swiper-slide-shadow-right {
  background-image: none;
}
.section .card {
  width: 40%;
  height: 90%;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 0 2em rgba(0, 0, 0, 0.2);
  padding: 2rem;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.section .card__image {
  width: 10em;
  height: 10em;
  border-radius: 50%;
  border: 5px solid var(--color);
  padding: 3px;
  margin-bottom: 2em;
}

.section .card__image img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
}

.section .card__content {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.section .card__title {
  font-size: 24px;
  font-weight: 900;
  position: relative;
  top: 0.2em;
}

.section .card__name {
  font-size: 16px;
  font-weight: 900;
  color: blue ! important;
}

.section .card__text {
  text-align: center;
  font-size: 1.1rem;
  margin: 1em 0;
}

.section .card__btn {
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
.section .breif {
  font-size: 16px;
}
</style>
