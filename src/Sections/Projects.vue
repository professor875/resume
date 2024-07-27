<script setup>
import Page from "@/components/Page.vue";

import img1 from "@/assets/images/project-4.jpg";
import img2 from "@/assets/images/project-5.jpg";
import img3 from "@/assets/images/project-1.jpg";
import img4 from "@/assets/images/project-2.jpg";
import img5 from "@/assets/images/project-6.jpg";
import img6 from "@/assets/images/project-3.jpg";

</script>

<template>
  <Page class="relative">
    <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
      <h1 class="background-heading left-[30%] top-[6%]">Projects</h1>
      <h2 data-aos="fade-up" class="text-center mb-[24px]">Our Projects</h2>
      <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">Far far away, behind the word mountains, far from
        the countries Vokalia and Consonantia</p>
    </div>

    <div class="grid sm:grid-cols-12 gap-6 md:gap-6">
      <div data-aos="fade-up" class="sm:col-span-4 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative"
           :style="{backgroundImage: `url(${img1})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
      <div data-aos="fade-up" class="sm:col-span-8 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative "
           :style="{backgroundImage: `url(${img2})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
      <div data-aos="fade-up" class="sm:col-span-8 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative"
           :style="{backgroundImage: `url(${img3})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
      <div data-aos="fade-up" class="sm:col-span-4 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative "
           :style="{backgroundImage: `url(${img4})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
      <div data-aos="fade-up" class="sm:col-span-8 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative"
           :style="{backgroundImage: `url(${img5})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
      <div data-aos="fade-up" class="sm:col-span-4 h-[200px] md:h-[300px] bg-cover bg-no-repeat bg-center relative "
           :style="{backgroundImage: `url(${img6})`}">
        <div
            class="absolute inset-0 flex flex-col justify-center items-center bg-[#FFBD39]/15 sm:bg-[#FFBD39]/75 sm:opacity-0 opacity-100 sm:hover:opacity-100 transition-opacity duration-300 px-10 space-y-2">
          <p class="text-center text-white text-[20px]">Branding & Illustration Design</p>
          <span class="text-center text-xs tracking-[3px] uppercase">web design</span>
        </div>
      </div>
    </div>
  </Page>
</template>