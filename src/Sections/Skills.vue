<script setup>
import Page from "@/components/Page.vue";

</script>

<template>
  <Page class="relative flex flex-col items-center">
    <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
      <h1 class="background-heading left-[35%] top-[17%]">Skills</h1>
      <h2 data-aos="fade-up" class="text-center mb-[24px]">My Skills</h2>
      <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">Far far away, behind the word mountains, far from the
        countries Vokalia and Consonantia</p>
    </div>

    <div data-aos="fade-up" class="grid sm:grid-cols-2 gap-4 md:gap-6 w-full">
      <!--      photoshop-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>Photoshop</span>
          <span class="left-[85%] absolute">90%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[90%]"></div>
        </div>
      </div>

      <!--      jQuery-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>JQuery</span>
          <span class="left-[80%] absolute">85%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[85%]"></div>
        </div>
      </div>

      <!--      HTML5-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>HTML5</span>
          <span class="left-[90%] absolute">95%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[95%]"></div>
        </div>
      </div>

      <!--      css3-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>CSS3</span>
          <span class="left-[85%] absolute">90%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[90%]"></div>
        </div>
      </div>

      <!--      wordpress-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>WordPress</span>
          <span class="left-[65%] absolute">70%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[70%]"></div>
        </div>
      </div>

      <!--      seo-->
      <div class="w-full">
        <div class="text-white text-[20px] w-full flex relative py-1">
          <span>SEO</span>
          <span class="left-[75%] absolute">80%</span>
        </div>
        <div class="relative w-full bg-secondary h-2 rounded-lg">
          <div class="absolute bg-primary h-2 rounded-lg w-[80%]"></div>
        </div>
      </div>
    </div>


  </Page>
</template>