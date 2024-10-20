<script setup>
const props = defineProps({
  title: {
    type: String,
    default: "PUT IN YOUR TITLE",
  },

  textContent: {
    type: String,
    default: "text content goes in here...",
  },
});
</script>

<template>
  <div>
    <h1
      class="font-[700] text-[16px] md:text-[24px] leading-[33.6px] mb-4 hidden lg:block"
    >
      {{ title }}
    </h1>
    <p
      class="text-center md:text-start font-[400] text-[10px] md:text-[18px] leading-[20px] md:leading-[27px] md:tracking-[-1.6%] md:w-[481px]"
    >
      {{ textContent }}
    </p>
  </div>
</template>
