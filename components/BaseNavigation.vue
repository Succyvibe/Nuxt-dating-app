<template>
  <div>
    <nav class="bg-[#fafafa] h-[60px] lg:h-[90px]">
      <div
        class="h-full container py-2 lg:py-0 px-4 mx-auto flex gap-[50px] items-center justify-between w-full"
      >
        <div class="flex gap-[60px]">
          <!-- ====logo==== -->
          <NuxtLink to="/"
            ><NuxtImg
              class="w-[100px] lg:w-[211.57px]"
              src="/icons/logo.png"
              alt="logo"
          /></NuxtLink>

          <!-- =======================NAV LINKS============ -->
          <ul
            class="flex flex-col items-center py-10 gap-y-6 lg:gap-y-0 lg:py-0 lg:flex-row lg:items-center md:gap-[20px] lg:gap-[40px] text-[10px] lg:text-[14px] xl:text-[22px] font-[500] leading-6"
          >
            <NuxtLink
              to="/about"
              class="'text-[10px]', 'lg:text-[14px]', 'xl:text-[22px]', 'font-[500]', 'leading-6', 'text-[black]',"
              >About</NuxtLink
            >

            <li>
              <NuxtLink to="/matches">Find Love</NuxtLink>
            </li>
            <li>
              <RouterLink to="/planView">Love & Be Loved</RouterLink>
            </li>
            <li>
              <NuxtLink to="/our-couple">Our Couples</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/contact">Contacts</NuxtLink>
            </li>
          </ul>
        </div>

        <ButtonComponent
          link="/matches"
          type="link"
          title="Find Match"
          bg="bg-[#FB1656]"
          class="hidden px-[10px] md:flex md:px-[60px] md:py-[6px]lg:py-[10px]"
        />
      </div>
    </nav>
  </div>
</template>

<style scoped>
@media (max-width: 720px) {
  .menu {
    position: absolute;
    top: 0;
    left: -200%;
    width: 80%;
    height: 100vh;
    background: #fb1656;
    transition: all 0.5s linear ease-in-out;
  }
}
</style>
