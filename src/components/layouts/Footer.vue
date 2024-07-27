<script setup>
import Page from "../Page.vue";
</script>

<template>
  <div class="py-[96px] md:py-[112px]">
    <Page data-aos="fade-up" class="grid md:grid-cols-4 gap-8">
      <div class="space-y-3 flex flex-col">
        <h3 class="font-semibold mb-4 md:mb-10">About</h3>
        <p>
          Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind
          texts.
        </p>

        <div class="flex gap-6 pt-4 sm:pt-10">
          <div class="size-12 flex justify-center items-center rounded-full bg-secondary text-[#A3A3A3]">
            <fa icon="fa-brands fa-twitter" size="xl"/>
          </div>
          <div class="size-12 flex justify-center items-center rounded-full bg-secondary text-[#A3A3A3]">
            <fa icon="fa-brands fa-facebook-f" size="xl"/>
          </div>
          <div class="size-12 flex justify-center items-center rounded-full bg-secondary text-[#A3A3A3]">
            <fa icon="fa-brands fa-instagram" size="xl"/>
          </div>
        </div>

      </div>
      <div class="space-y-3 flex flex-col">
        <h3 class="font-semibold mb-4 md:mb-10">Links</h3>

        <a class="text-[#999999]" href="#home">
          <fa icon="fa-solid fa-arrow-right-long"/>
          Home</a>
        <a class="text-[#999999]" href="#about">
          <fa icon="fa-solid fa-arrow-right-long"/>
          About</a>
        <a class="text-[#999999]" href="#services">
          <fa icon="fa-solid fa-arrow-right-long"/>
          Services</a>
        <a class="text-[#999999]" href="#projects">
          <fa icon="fa-solid fa-arrow-right-long"/>
          Projects</a>
        <a class="text-[#999999]" href="#contact">
          <fa icon="fa-solid fa-arrow-right-long"/>
          Contact</a>
      </div>
      <div class="space-y-3 flex flex-col">
        <h3 class="font-semibold mb-4 md:mb-10">Services</h3>

        <a href="#services">
          <p>
            <fa icon="fa-solid fa-arrow-right-long"/>
            Web Design
          </p>
          <p>
            <fa icon="fa-solid fa-arrow-right-long"/>
            Web Development
          </p>
          <p>
            <fa icon="fa-solid fa-arrow-right-long"/>
            Business Strategy
          </p>
          <p>
            <fa icon="fa-solid fa-arrow-right-long"/>
            Data Analysis
          </p>
          <p>
            <fa icon="fa-solid fa-arrow-right-long"/>
            Graphic Design
          </p>
        </a>
      </div>
      <div class="space-y-5 flex flex-col">
        <h3 class="font-semibold mb-4 md:mb-10">About</h3>

        <span class="space-x-4 flex items-start"><fa icon="fa-solid fa-location-dot"/><p class="-mt-2"> 203 Fake St. Mountain View, San Francisco, California, USA</p></span>
        <span class="space-x-4 flex items-start text-[#999999]"><fa icon="fa-solid fa-phone"/><p class="-mt-2"> +2 392 3929 210</p></span>
        <span class="space-x-4 flex items-start text-[#999999]"><fa icon="fa-solid fa-envelope"/><p class="-mt-2"> info@yourdomain.com</p></span>
      </div>
    </Page>

    <p data-aos="fade-up" class="text-center pb-16 pt-16">Copyright ©2024 All rights reserved | made with
      <fa style="color:white" icon="fa-solid fa-heart"/>
      by
      <a href="https://github.com/code-creeper/" target="_blank"
         class="text-white cursor-pointer hover:text-[#999999] transition-all duration-300">Code Creeper</a></p>
  </div>
</template>