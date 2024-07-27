<script setup>
import Navbar from '@/components/layouts/Navbar.vue'
import Home from "@/Sections/Home.vue";
import About from "@/Sections/About.vue";
import Resume from "@/Sections/Resume.vue";
import Projects from "@/Sections/Projects.vue";
import Blog from "@/Sections/Blog.vue";
import Contact from "@/Sections/Contact.vue";
import Footer from "@/components/layouts/Footer.vue";
import Skills from "@/Sections/Skills.vue";
import Services from "@/Sections/Services.vue";
import {onMounted, onUnmounted, ref} from "vue";

const activeSectionName = ref('home')

const homeRef = ref(null);
const aboutRef = ref(null);
const resumeRef = ref(null);
const servicesRef = ref(null);
const skillsRef = ref(null);
const projectsRef = ref(null);
const blogRef = ref(null);
const contactRef = ref(null);

const handleHashChange = () => {
  const refs = {
    home: homeRef,
    about: aboutRef,
    resume: resumeRef,
    services: servicesRef,
    skills: skillsRef,
    projects: projectsRef,
    blog: blogRef,
    contact: contactRef,
  }

  const hash = window.location.hash.slice(1);

  if (refs[hash] && refs[hash].value) {
    refs[hash].value.scrollIntoView({behavior: 'smooth'});
  }
}

const handleScroll = () => {
  const sections = [
    {ref: homeRef, name: 'home'},
    {ref: aboutRef, name: 'about'},
    {ref: resumeRef, name: 'resume'},
    {ref: servicesRef, name: 'services'},
    {ref: skillsRef, name: 'skills'},
    {ref: projectsRef, name: 'projects'},
    {ref: blogRef, name: 'blog'},
    {ref: contactRef, name: 'contact'},
  ];

  const scrollTop = window.scrollY;
  const offset = window.innerHeight / 3;

  for (const section of sections) {
    const element = section.ref.value;
    if (element) {
      const rect = element.getBoundingClientRect();
      if (rect.top >= -offset && rect.top < window.innerHeight - offset) {
        activeSectionName.value = section.name;
        break;
      }
    }
  }
}

onMounted(() => {
  handleHashChange();

  window.addEventListener('hashchange', handleHashChange)
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('hashchange', handleHashChange);
  window.removeEventListener('scroll', handleScroll);
})
</script>

<template>
  <Navbar :activeSectionName="activeSectionName"/>
  <div ref="homeRef">
    <Home/>
  </div>
  <div class="pt-[96px] md:pt-[112px]" ref="aboutRef">
    <About/>
  </div>
  <div class="pt-[96px] md:pt-[112px]" ref="resumeRef">
    <Resume/>
  </div>
  <div class="pt-[96px] md:pt-[112px]" ref="servicesRef">
    <Services/>
  </div>
  <div class="py-[96px] md:py-[112px]" ref="skillsRef">
    <Skills/>
  </div>
  <div class="py-[96px] md:py-[112px]" ref="projectsRef">
    <Projects/>
  </div>
  <div class="py-[96px] md:py-[112px]" ref="blogRef">
    <Blog/>
  </div>
  <div class="pt-[96px] md:pt-[112px]" ref="contactRef">
    <Contact/>
  </div>
  <Footer/>

</template>