<script setup>
import Page from "@/components/Page.vue";
</script>

<template>
  <Page>
    <div class="w-full flex relative">
      <h1 class="background-heading left-[46%] top-[5%]">About</h1>
      <div class="hidden md:inline max-w-[500px]">
        <img src="../assets/images/hero-1.png" alt="hero-1">
      </div>

      <div class="space-y-10">
        <h2 data-aos="fade-up">About Me</h2>
        <p data-aos="fade-up">A small river named Duden flows by their place and supplies it with the necessary regelialia.</p>
        <table data-aos="fade-up">
          <tr>
            <td class='font-semibold text-white'>Name:</td>
            <td>Clark Thompson</td>
          </tr>
          <tr>
            <td class='font-semibold text-white'>Date of birth:</td>
            <td>January 01, 1987</td>
          </tr>
          <tr>
            <td class='font-semibold text-white'>Address:</td>
            <td>San Francisco CA 97987 USA</td>
          </tr>
          <tr>
            <td class='font-semibold text-white'>Zip code:</td>
            <td>1000</td>
          </tr>
          <tr>
            <td class='font-semibold text-white'>Email:</td>
            <td>clarkthomp@gmail.com</td>
          </tr>
          <tr>
            <td class='font-semibold text-white'>Phone:</td>
            <td>+1-2234-5678-9-0</td>
          </tr>
        </table>
        <p data-aos="fade-up" class="text-[20px] text-white"><span class="text-primary font-semibold">120</span> Project complete</p>

        <button data-aos="fade-up" class="p-[16px] border border-primary text-black text-[12px] font-[600] tracking-[2px] bg-primary rounded-full uppercase ">download cv</button>
      </div>
    </div>
  </Page>
</template>

<style scoped>
table {
  color: #999999;
  max-width: 400px;
  width: 100%;
}

tr {
  border-bottom: 10px solid transparent;
}
</style>