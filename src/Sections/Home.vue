<script setup>
import {Swiper, SwiperSlide} from 'swiper/vue';
import { Autoplay, Pagination } from 'swiper/modules';

const pagination = {
  clickable: true,
      renderBullet: function (index, className) {
    return '<span class="' + className + '"></span>';
  },
};
const modules = [Autoplay, Pagination]
</script>

<template>
  <swiper
      :pagination="pagination" :modules="modules"
      :slides-per-view="1"
      :loop="true"
      :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
  >
    <swiper-slide>
        <div
            class="max-w-[1140px] mx-auto px-[10px] md:px-[50px] container bg-overlay flex justify-center md:justify-start items-center min-h-[750px]">
          <div class="md:max-w-[600px] space-y-8 w-full">
            <p class="text-primary uppercase tracking-[3px] text-[14px] text-center md:text-start w-full">hello!</p>
            <h1 class="text-center md:text-start">
              I'm <span class="text-primary">Clark Thompson</span>
            </h1>
            <p class="text-[30px] font-light text-center md:text-start">A Freelance Web Designer</p>

            <div class="space-x-2 mx-auto md:mx-0 flex justify-center md:justify-start">
              <button class="py-[16px] px-[24px] bg-primary rounded-full text-black cursor-default">Hire me</button>
              <button class="py-[16px] px-[24px] border rounded-full cursor-default">My works</button>
            </div>
          </div>
        </div>
    </swiper-slide>
    <swiper-slide>
        <div
            class="max-w-[1140px] mx-auto px-[10px] md:px-[50px] container-2 bg-overlay flex justify-center md:justify-start items-center min-h-[750px]">
          <div class="md:max-w-[500px] space-y-8">
            <p class="text-primary uppercase tracking-[3px] text-[14px] w-full text-center md:text-start">hello!</p>
            <h1 class="text-center md:text-start">
              I'm a <span class="text-primary text-center md:text-start">web designer</span> based in London
            </h1>
            <div class="space-x-2 flex justify-center md:justify-start">
              <button class="py-[16px] px-[24px] bg-primary rounded-full text-black cursor-default">Hire me</button>
              <button class="py-[16px] px-[24px] border rounded-full cursor-default">My works</button>
            </div>
          </div>
        </div>
    </swiper-slide>
  </swiper>
</template>

<style scoped>
.container, .container-2 {
  background-repeat: no-repeat;
  background-size: 80%;
  background-position: 140% 10%;
}

.container {
  background-image: url("../assets/images/hero-1.png");
}

.container-2 {
  background-image: url("../assets/images/hero-2.png");
}

.bg-overlay {
  border-image-source: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.5));
}

@media (max-width: 767px) {
  .container, .container-2 {
    background-position: center;
    background-size: cover;
  }

  .bg-overlay {
    border-image-slice: fill 1;
  }
}
</style>