<template>
  <div>
    <BaseHeader />
    <!-- <BaseNavigation /> -->
    <Navigation />
    <div>
      <slot />
    </div>

    <footer class="bg-[#7D0B2B]">
      <div class="container mx-auto px-4 lg:px-[160px] lg:py-[40px]">
        <div
          class="grid xl:flex items-center justify-between text-white xl:gap-20 pt-10"
        >
          <div>
            <img src="/icons/msgIcon.png" alt="" class="w-[30px] xl:w-[65px]" />
            <p class="text-[10px] mt-4">
              Talk, Connect, Fall in Love – Your Journey Starts Here
            </p>
          </div>

          <div>
            <h5 class="mb-8 font-[700]">Product</h5>

            <ul class="text-[10px] xl:text-[16px] font-[400]">
              <li>
                <NuxtLink href="#">Pricing</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Sign in</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Documentation</NuxtLink>
              </li>
            </ul>
          </div>
          <div>
            <h5 class="mb-8 font-[700]">Company</h5>

            <ul class="text-[10px] xl:text-[16px] font-[400]">
              <li>
                <NuxtLink href="#">Pricing</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Sign in</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Documentation</NuxtLink>
              </li>
            </ul>
          </div>
          <div>
            <h5 class="mb-8 font-[700]">Legal</h5>

            <ul class="text-[10px] xl:text-[16px] font-[400]">
              <li>
                <NuxtLink href="#">Pricing</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Sign in</NuxtLink>
              </li>
              <li>
                <NuxtLink href="#">Documentation</NuxtLink>
              </li>
            </ul>
          </div>

          <ul class="flex flex-col gap-y-5">
            <li>
              <a href="">
                <NuxtImg src="/icons/twitter.png" alt="" />
              </a>
            </li>
            <li>
              <a href="">
                <NuxtImg src="/icons/twitter.png" alt="" />
              </a>
            </li>
            <li>
              <a href="">
                <NuxtImg src="/icons/twitter.png" alt="" />
              </a>
            </li>
          </ul>
        </div>
        <p class="text-[12px] leading-[18px] text-white">
          © Copyright 2024, All Rights Reserved by Aditama
        </p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
@media (max-width: 560px) {
  .btn {
    display: none;
  }
}
</style>
