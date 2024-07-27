<script setup>
import Page from "@/components/Page.vue";
import {reactive, ref} from "vue";
import * as emailjs from "@emailjs/browser";

const form = reactive({
  name: "",
  email: "",
  subject: "",
  message: "",
})

const errors = reactive({})

const loading = ref(false)

const handleSubmit = () => {
  resetObject(errors)
  loading.value = true
  let validated = validate(form);

  if (validated) {
    emailjs
        .send('service_al2esak', 'template_51hsher', form, {
          publicKey: '9_wg9qTIg4JubuW8o',
        })
        .then(
            () => {
              alert('Your Message has been sent!');
            }
        )
        .catch(() => {
          alert('Something went wrong!');
        });
    resetObject(form)
    loading.value = false
  } else {
    loading.value = false
  }
}

const validate = (form) => {
  let error = false;

  if (form.name === '') {
    errors.name = "Name field is Required"
    error = true
  }
  if (form.email === '') {
    errors.email = "Email field is Required"
    error = true
  }
  if (form.subject === '') {
    errors.subject = "Subject field is Required"
    error = true
  }
  if (form.message === '') {
    errors.message = "Message field is Required"
    error = true
  }
  return !error;
}

const resetObject = (object) => {
  Object.keys(object).forEach(key => {
    object[key] = '';
  });
}

const information = [
  {
    icon: 'fa-solid fa-map',
    title: 'Address',
    info: '198 West 21th Street, Suite 721 New York NY 10016',
  },
  {
    icon: 'fa-solid fa-address-book',
    title: 'contact number',
    info: '+ 1235 2355 98',
  },
  {
    icon: 'fa-solid fa-envelope',
    title: 'email address',
    info: 'info@yoursite.com',
  },
  {
    icon: 'fa-solid fa-sitemap',
    title: 'website',
    info: 'yoursite.com',
  },
]
</script>

<template>
  <Page class="relative">
    <div class="mx-[15px] md:mx-0 pb-[48px] md:px-[15px]">
      <h1 class="background-heading left-[28%] top-[6%]">Contact</h1>
      <h2 data-aos="fade-up" class="text-center mb-[24px]">Contact Me</h2>
      <p data-aos="fade-up" class="text-center max-w-[950px] mx-auto mb-[16px]">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
    </div>

    <div data-aos="fade-up" class="grid sm:grid-cols-2 md:grid-cols-4 gap-6 pb-[120px]">
      <div class="w-full flex flex-col items-center justify-start gap-4" v-for="(data, index) in information" :key="index">
        <div class="bg-secondary text-primary rounded-full p-10">
          <fa :icon="data.icon" size="2xl"/>
        </div>
        <h4 class="text-[17px] text-center font-normal uppercase">{{ data.title }}</h4>
        <p class="text-center max-w-[200px]" :class="index !== 0 && 'text-white'">{{ data.info }}</p>
      </div>
    </div>

    <div data-aos="fade-up" class="w-full flex flex-col-reverse md:grid md:grid-cols-2">
      <div class="h-full w-full">
        <img class="w-full h-full object-cover" src="../assets/images/bg-2.jpg" alt="bg-2">
      </div>
      <div class="bg-[#F8F9FA] p-6 md:p-[50px] w-full text-black">
        <form @submit.prevent="handleSubmit" class="space-y-4">
          <div>
            <input
                class="w-full p-4 rounded-md border border-gray-400 text-[14px] focus:outline-0 focus:border-gray-600"
                v-model="form.name" name="name" type="text" placeholder="Your Name"/>
            <p class="text-xs text-red-500 py-1">{{ errors.name ?? '' }}</p>
          </div>
          <div>
            <input
                class="w-full p-4 rounded-md border border-gray-400 text-[14px] focus:outline-0 focus:border-gray-600"
                v-model="form.email" name="email" type="text" placeholder="Your Email"/>
            <p class="text-xs text-red-500 py-1">{{ errors.email ?? '' }}</p>
          </div>
          <div>
            <input
                class="w-full p-4 rounded-md border border-gray-400 text-[14px] focus:outline-0 focus:border-gray-600"
                v-model="form.subject" name="subject" type="text" placeholder="Your Subject"/>
            <p class="text-xs text-red-500 py-1">{{ errors.subject ?? '' }}</p>
          </div>

          <div>
            <textarea v-model="form.message"
                      placeholder="Message"
                      class="w-full rounded-md p-4 text-[14px] border border-gray-400 focus:outline-0 focus:border-gray-600"
                      name="message" rows="10"></textarea>
            <p class="text-xs text-red-500">{{ errors.message ?? '' }}</p>
          </div>

          <button class="font-[600] bg-primary rounded-full w-full sm:w-auto px-[48px] py-[16px] text-[12px] tracking-[2px] uppercase"
                  :class="loading && 'opacity-70 cursor-progress'" :disabled="loading">send
            message
          </button>
        </form>
      </div>
    </div>
  </Page>
</template>