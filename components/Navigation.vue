<script setup>
import { onMounted, ref } from "vue";

let scrollNav = ref(null);
let mobile = ref(false);
let mobileNav = ref(null);
let windowWidth = ref(null);
const route = useRoute();

const toggleMobileNav = () => {
  mobileNav.value = !mobileNav.value;
};

watch(route, () => {
  mobileNav.value = false;
});

const updateScroll = () => {
  const scrollPosition = window.scrollY;
  if (scrollPosition > 50) {
    scrollNav.value = true;
    return;
  }

  scrollNav.value = false;
};

const checkScreen = () => {
  windowWidth.value = window.innerWidth;
  console.log(windowWidth.value);
  if (windowWidth.value <= 780) {
    console.log("On size 740");
    mobile.value = true;
    return;
  }

  console.log("Not size");
  mobile.value = false;
  mobileNav.value = false;
  return;
};

onMounted(() => {
  window.addEventListener("scroll", updateScroll);

  console.log("Its' scrolling");
});
onMounted(() => {
  window.addEventListener("resize", checkScreen);
  checkScreen();
  console.log("It's resizing");
});
</script>

<template>
  <nav class="bg-[#fafafa] shadow-md lg:shadow-none relative py-3">
    <div class="navbar container mx-auto flex">
      <NuxtLink to="/"
        ><NuxtImg
          class="w-[100px] lg:w-[211.57px]"
          src="/icons/logo.png"
          alt="logo"
      /></NuxtLink>

      <ul
        v-show="!mobile"
        class="hidden navigation lg:flex items-center font-[500] leading-6 ml-[40px] text-[18px] transition-all ease-in-out duration-[0.5s]"
      >
        <li class="ml-[20px] hover:text-[red]">
          <NuxtLink
            to="/about"
            class="'text-[10px]', 'lg:text-[14px]', 'xl:text-[22px]', 'font-[500]', 'leading-6', 'text-[black]',"
            >Portfolio</NuxtLink
          >
        </li>

        <li class="ml-[20px] hover:text-[red]">
          <NuxtLink to="/matches">Find Love</NuxtLink>
        </li>
        <li class="ml-[20px] hover:text-[red]">
          <RouterLink to="/planView">Love & Be Loved</RouterLink>
        </li>
        <li class="ml-[20px] hover:text-[red]">
          <NuxtLink to="/our-couple">Our Couples</NuxtLink>
        </li>
        <li class="ml-[20px] hover:text-[red]">
          <NuxtLink to="/contact">Contacts</NuxtLink>
        </li>
      </ul>

      <div class="hidden lg:flex-1 lg:flex lg:justify-end lg:items-center">
        <NuxtLink to="/matches">
          <ButtonComponent
            link="/matches"
            type="link"
            title="Find Match"
            bg="bg-[#FB1656]"
            class="px-[10px] md:flex md:px-[60px] md:py-[6px]lg:py-[10px]"
          />
        </NuxtLink>
      </div>

      <div class="">
        <i
          class="fa-solid fa-bars cursor-pointer absolute top-[18px] right-[10%]"
          v-show="mobile"
          :class="{ 'icon-active': mobileNav }"
          @click="toggleMobileNav"
        ></i>
      </div>
      <transition name="mobile-nav">
        <ul
          v-show="mobileNav"
          class="dropdown-nav fixed top-0 left-0 z-40 w-[250px] h-[100vh] bg-[#fb1656] flex flex-col items-center pt-20 gap-y-8 font-[500] leading-6 text-[18px] transition-all ease-in-out duration-[0.5s] lg:hidden text-[#fff]"
        >
          <li class="ml-[20px] hover:border-b">
            <NuxtLink
              to="/about"
              class="'text-[10px]', 'lg:text-[14px]', 'xl:text-[22px]', 'font-[500]', 'leading-6', 'text-[black]',"
              >Portfolio</NuxtLink
            >
          </li>

          <li class="ml-[20px] hover:border-b">
            <NuxtLink
              class="hover:border-b hover:border-b-[white]"
              to="/matches"
              >Find Love</NuxtLink
            >
          </li>
          <li class="ml-[20px] hover:border-b">
            <NuxtLink
              class="hover:border-b hover:border-b-[white]"
              to="/planView"
              >Love & Be Loved</NuxtLink
            >
          </li>
          <li class="ml-[20px] hover:border-b">
            <NuxtLink
              class="hover:border-b hover:border-b-[white]"
              to="/our-couple"
              >Our Couples</NuxtLink
            >
          </li>
          <li class="ml-[20px] hover:border-b">
            <NuxtLink
              class="hover:border-b hover:border-b-[white]"
              to="/contact"
              >Contacts</NuxtLink
            >
          </li>
        </ul>
      </transition>
    </div>
  </nav>
</template>

<style scoped>
.icon-active {
  transform: rotate(180deg);
}

.mobile-nav-enter-active {
  transition: 1s ease all;
}
.mobile-nav-leave-active {
  transition: 1s ease all;
}

.mobile-nav-enter-from {
  transform: translateX(-250px);
}

.mobile-nav-leave-to {
  transform: translateX(-250px);
}

.mobile-nav-enter-to {
  transform: translateX(0);
}

.slideOut {
  transform: translateX(-250px);
}
.slideIn {
  transform: translateX(0);
}
</style>
