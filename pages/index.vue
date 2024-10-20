<script setup lang="ts">
useHead({
  title: "My Dating App",
  meta: [{ name: "description", content: "My amazing site." }],
  bodyAttrs: {
    class: "test",
  },
  script: [{ innerHTML: "console.log('Hello world')" }],
});
</script>

<template>
  <div>
    <HeroSection />
    <Results />
    <About />
    <FindMatch />
    <Testimonial />
    <PricingPlan />
    <MeetLove />
  </div>
</template>
