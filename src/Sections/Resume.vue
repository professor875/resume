<script setup>
import Page from "@/components/Page.vue";

const resume = [
  {
    year: '2014-2015',
    degree: 'Master Degree of Design',
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.',
  },
  {
    year: '2014-2015',
    degree: 'Art & Creative Director',
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.',
  },
  {
    year: '2014-2015',
    degree: "Bachelor's Degree of C.A",
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted part s of sentences fly into your mouth.',
  },
  {
    year: '2014-2015',
    degree: 'Wordpress Developer',
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.',
  },
  {
    year: '2014-2015',
    degree: 'Diploma in Computer',
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.',
  },
  {
    year: '2017-2018',
    degree: 'UI/UX Designer',
    university: 'CAMBRIDGE UNIVERSITY',
    description: 'A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.',
  },
]
</script>

<template>
  <Page class="relative flex flex-col items-center">
    <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
      <h1 class="background-heading left-[30%] top-[5%]">Resume</h1>
      <h2 data-aos="fade-up" class="text-center mb-[24px]">Resume</h2>
      <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">A small river named Duden flows by their place and supplies
        it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full mb-[70px]">
      <div data-aos="fade-up" v-for="(data, index) in resume" :key="index" class="p-[30px] bg-secondary space-y-1">
        <h3 class="font-bold text-primary">{{ data.year }}</h3>
        <h3>{{ data.degree }}</h3>
        <p class="text-[12px] uppercase tracking-[3px]">{{ data.university }}</p>
        <p class="my-3">{{ data.description }}</p>
      </div>
    </div>

    <button data-aos="fade-up"
            class="bg-primary font-[600] text-black px-[48px] py-[24px] rounded-full uppercase tracking-[2px] text-[12px] mx-auto">
      download cv
    </button>
  </Page>
</template>