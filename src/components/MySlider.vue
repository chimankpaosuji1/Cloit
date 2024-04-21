<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide">Slide 1</div>
      <div class="swiper-slide">Slide 2</div>
      <div class="swiper-slide">Slide 3</div>
      <!-- Add more slides as needed -->
    </div>
    <!-- Pagination -->
    <div class="swiper-pagination"></div>
    <!-- Navigation buttons -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';

export default {
  name: "MySlider",
  mounted() {
    new Swiper('.swiper-container', {
      slidesPerView: 3,
      centeredSlides: true,
      spaceBetween: -80, // Adjust the space between slides as needed
      loop: true,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
    });
  }
}
</script>

<style scoped>
/* Custom styles for the swiper container */
.swiper-container {
  width: 100%;
  height: 300px; /* Adjust height as needed */
  position: relative; /* Required for absolute positioning of pagination and navigation */
}

/* Custom styles for the swiper slides */
.swiper-slide {
  width: 200px; /* Adjust slide width as needed */
  height: 200px; /* Adjust slide height as needed */
  background-color: #ccc; /* Example background color */
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 24px;
  border-radius: 10px; /* Add border-radius for rounded corners */
}

/* Custom styles for the pagination */
.swiper-pagination {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
}

/* Custom styles for the navigation buttons */
.swiper-button-next,
.swiper-button-prev {
  color: #fff; /* Example color */
  background-color: #007bff; /* Example background color */
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10; /* Ensure navigation buttons appear above slides */
}

.swiper-button-next {
  right: 10px;
}

.swiper-button-prev {
  left: 10px;
}
</style>