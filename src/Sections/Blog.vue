<script setup>
import Page from "@/components/Page.vue";

import img1 from "@/assets/images/image_1.jpg";
import img2 from "@/assets/images/image_2.jpg";
import img3 from "@/assets/images/image_3.jpg";
import bgImg from "@/assets/images/bg_1.jpg";

const blogs = [
  {
    img: img1,
    date: 'JUNE 21, 2019 ADMIN',
    heading: 'Why Lead Generation is Key for Business Growth',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
  },
  {
    img: img2,
    date: 'JUNE 21, 2019 ADMIN',
    heading: 'Why Lead Generation is Key for Business Growth',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
  },
  {
    img: img3,
    date: 'JUNE 21, 2019 ADMIN',
    heading: 'Why Lead Generation is Key for Business Growth',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
  },
]

const status = [
  {
    number: '100',
    heading: 'Awards',
  },
  {
    number: '1,200',
    heading: 'Complete Projects',
  },
  {
    number: '1,200',
    heading: 'Happy Customers',
  },
  {
    number: '500',
    heading: 'Cups of coffee',
  },
]
</script>

<template>
  <div>
    <Page class="relative">
      <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
        <h1 class="background-heading left-[38%] top-[7%]">Blog</h1>
        <h2 data-aos="fade-up" class="text-center mb-[24px]">Our Blog</h2>
        <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div data-aos="fade-up" :key="index" class="space-y-4" v-for="(blog, index) in blogs">
          <div class="h-[250px] md:h-[350px] w-full bg-no-repeat bg-cover bg-center cursor-pointer"
               :style="{backgroundImage: `url(${blog.img})`}"></div>
          <p class="text-primary text-[12px] tracking-[3px] uppercase cursor-pointer">{{ blog.date }}</p>

          <a class="text-[20px] text-white hover:text-primary transition-colors duration-300 cursor-pointer">{{
              blog.heading
            }}</a>
          <p>{{ blog.description }}</p>
        </div>
      </div>

      <div
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 sm:gap-12 justify-center items-center translate-y-[80px] relative z-10">
        <div data-aos="fade-up"
             class="h-[140px] sm:h-[170px] px-12 w-full flex flex-col justify-center items-center bg-secondary gap-3 mx-auto"
             v-for="(data, index) in status">
          <span class="text-[30px] font-bold text-primary text-center">{{ data.number }}</span>
          <p class="text-white text-center">{{ data.heading }}</p>
        </div>
      </div>
    </Page>

    <div data-aos="fade-up"
         class="w-full min-h-[500px] bg-no-repeat bg-cover bg-center flex flex-col justify-end items-center gap-6 md:gap-12 p-10"
         :style="{backgroundImage: `url(${bgImg})`}">
      <h2>I'm <span class="text-primary">Available</span> for freelancing</h2>
      <p>A small river named Duden flows by their place and supplies it with the necessary regelialia.</p>
      <button
          class="bg-primary rounded-full text-black text-[12px] tracking-[2px] uppercase py-[16px] px-[48px] border border-primary cursor-default font-[600]">
        hire me
      </button>
    </div>
  </div>
</template>