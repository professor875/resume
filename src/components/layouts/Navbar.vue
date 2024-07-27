<script setup>
import {ref} from "vue";

defineProps({
  activeSectionName: String
})

const navLinks = [
  {
    label: "Home",
    href: "#home",
    name: "home",
  },
  {
    label: "About",
    href: "#about",
    name: "about",
  },
  {
    label: "Resume",
    href: "#resume",
    name: "resume",
  },
  {
    label: "Services",
    href: "#services",
    name: "services",
  },
  {
    label: "Skills",
    href: "#skills",
    name: "skills",
  },
  {
    label: "Projects",
    href: "#projects",
    name: "projects",
  },
  {
    label: "Blog",
    href: "#blog",
    name: "blog",
  },
  {
    label: "Contact",
    href: "#contact",
    name: "contact",
  },
]
const activated = ref(false)

const toggle = () => {
  activated.value = !activated.value
}

</script>

<template>
  <div :class="activeSectionName !== 'home' && 'navShow'">
    <nav :class="activeSectionName !== 'home' && 'bg-black'"
        class="max-w-[1140px] mx-auto px-[10px] md:px-[50px] flex w-full justify-between gap-3 items-center py-3">
      <a class="uppercase text-white text-[24px] font-black" href="#">clark</a>

      <!--      desktop Nav-->
      <div class="hidden md:inline-flex w-full justify-between max-w-[750px] text-[16px]">
        <a v-for="(link, index) in navLinks" :href="link.href" class="px-2 py-2 link relative" :class="{'active-link': activeSectionName === link.name}" :key="index">{{
            link.label
          }}</a>
      </div>

      <!--      MobileNav-->
      <div @click="toggle" class="md:hidden flex gap-2 items-center px-6 py-2 cursor-pointer">
        <div class="hamburger w-[20px] border-[1px] border-[#7C7C7C] relative"></div>
        <span class="text-[16px] text-[#7C7C7C] uppercase">Menu</span>
      </div>
    </nav>

    <!--    mobile navlinks list-->
    <div :class="`gap-2 flex flex-col overflow-hidden max-h-0 ${activated === true ? 'toogle-on' : 'toogle-off'}`">
      <a
          @click="toggle"
          v-for="(link, index) in navLinks"
          :href="link.href"
          class="px-2 py-2 mobile-link relative w-full"
          :key="index"
          :class="{'active-mobile-link': activeSectionName === link.name}"
      >{{
          link.label
        }}</a>
    </div>
  </div>

</template>

<style scoped>
@media (min-width: 767px) {
  .navShow {
    position: sticky;
    top: 0;
    z-index: 50;
    background-color: black;
    animation: slideDown 0.3s forwards;
  }
}

@keyframes slideDown {
  from{ transform: translateY(-100%); }
  to{ transform: translateY(0); }
}

.link::before {
  content: "";
  position: absolute;
  width: 0;
  bottom: 0;
  right: 50%;
  border-color: var(--primary-color);
  transition: 300ms;
}

.link:hover::before {
  width: 80%;
  border: 1px solid var(--primary-color);
  right: 9%;
}

.active-link {
  color: var(--primary-color);
}

.active-link::before {
  content: '';
  width: 80%;
  border: 1px solid;
  right: 9%;
}

/*mobile Nav*/
.hamburger::after {
  content: '';
  position: absolute;
  width: 20px;
  border: 1px solid #7C7C7C;
  top: 6px;
  left: -1px;
}

.hamburger::before {
  content: '';
  position: absolute;
  width: 20px;
  border: 1px solid #7C7C7C;
  top: -8px;
  left: -1px;
}

.mobile-link::before {
  content: "";
  position: absolute;
  width: 0;
  bottom: 0;
  left: 35px;
  border-color: var(--primary-color);
  transition: 300ms;
}

.mobile-link:hover::before {
  width: 75px;
  border: 1px solid var(--primary-color);
  left: 5px;
}

.active-mobile-link {
  color: var(--primary-color);
}

.active-mobile-link::before {
  content: '';
  width: 75px;
  border: 1px solid;
  left: 5px;
}
.toogle-on {
  max-height: 500px;
  transition: max-height 0.5s ease;
}
.toogle-off{
  max-height: 0;
  transition: max-height 0.5s ease;
}
</style>