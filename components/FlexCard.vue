<script setup>
const props = defineProps({
  display: {
    type: String,
    default: "flex",
  },
});
</script>

<template>
  <div>
    <div
      :class="`${display} container mx-auto px-4 lg:pt-[40px] lg:pr-[160px] lg:pb-[160px] lg:pl-[160px] flex-col items-center lg:items-center lg:flex-row lg:justify-between gap-7 lg:gap-0 lg:my-20`"
    >
      <img src="/images/aboutImage.png" alt="" />

      <TextCard
        title="About Us"
        textContent=" Welcome to Love Flow, where love meets innovation. Our mission is to
          create meaningful connections that lead to real-life relationships. We
          believe that everyone deserves to find their perfect match, and our
          app is designed to make that journey as seamless and enjoyable as
          possible. Welcome to Love Flow, where love meets innovation. Our
          mission is to create meaningful connections that lead to real-life
          relationships. We believe that everyone deserves to find their perfect
          match, and our app is designed to make that journey as seamless and
          enjoyable as possible."
      />
    </div>
  </div>
</template>
