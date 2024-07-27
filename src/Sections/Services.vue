<script setup>
import Page from "@/components/Page.vue";

const services = [
  {
    icon: 'fa-solid fa-wand-magic-sparkles',
    title: 'web design',
  },
  {
    icon: 'fa-solid fa-flask-vial',
    title: 'photography',
  },
  {
    icon: 'fa-solid fa-code',
    title: 'web developer',
  },
  {
    icon: 'fa-solid fa-soap',
    title: 'app developing',
  },
  {
    icon: 'fa-solid fa-ranking-star',
    title: 'branding',
  },
  {
    icon: 'fa-solid fa-chart-line',
    title: 'product strategy',
  },
]

</script>

<template>
  <Page class="relative flex flex-col items-center">
    <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
      <h1 class="background-heading left-[27%] top-[10%]">Services</h1>
      <h2 data-aos="fade-up" class="text-center mb-[24px]">Services</h2>
      <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">Far far away, behind the word mountains, far from the
        countries Vokalia and Consonantia</p>
    </div>

    <div class="grid px-10 sm:px-4 sm:grid-cols-3 gap-8 w-full">
      <div data-aos="fade-up" class="w-full min-h-[220px] bg-secondary flex flex-col justify-center items-center gap-5 p-[32px] transition-colors duration-300 group hover:bg-primary"
           v-for="(service, index) in services" :key="index">
        <div class="text-primary transition-all duration-300 group-hover:text-white">
          <fa :icon="service.icon" size="3x"/>
        </div>
        <p class="text-white transition-all duration-300 group-hover:text-black tracking-[2px] text-[13px] uppercase font-[500] text-center">{{ service.title }}</p>
        <hr class="w-10 border border-primary transition-all duration-300 group-hover:border-black">
      </div>
    </div>
  </Page>
</template>