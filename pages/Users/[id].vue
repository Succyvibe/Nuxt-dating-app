<!-- /matches/id -->

<script setup>
const { id } = useRoute().params;

const { data, error } = await useFetch(`https://dummyjson.com/data?./${id}`);
</script>

<template>
  <section>
    <div class="w-[90%] xl:w-[1120px] mx-auto xl:p-20">
      <div class="w-full grid xl:grid-cols-2 gap-4">
        <!-- ==================col 1==================== -->
        <div>
          <div class="w-full h-[356px]">
            <NuxtImg
              class="w-full h-full rounded-[24px] object-cover"
              :src="data?.image"
              alt=""
            />
          </div>
          <div class="pt-5">
            <p
              class="text-center font-Poppins text-[15px] lg:text-[18px] font-[700] leading-[21px] tracking-[-1.6%] text-[#454747]"
            >
              <span>{{ data?.firstName }}</span>
              <span class="mx-2">{{ data?.lastName }}</span>
              <span>{{ data?.age }}</span>
            </p>
            <!-- ==============City======== -->
            <p
              class="text-[18px] text-[#454747] font-[300] leading-[27px] tracking-[-1.6%]"
            >
              {{ data?.address.state }}
            </p>
            <p
              class="text-[14px] leading-[21px] text-[#000000] tracking-[-0.6%] my-5"
            >
              Works as an ${{ data?.company.department }}
            </p>
          </div>

          <ul
            class="text-[16px] font-Poppins font-[400] leading-[24px] tracking-[-1.2%] text-[#7D0B2B] flex-wrap flex gap-[10px]"
          >
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Drinking</li>
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Dancing</li>
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Local Culture</li>
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Recreation</li>
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Swimming</li>
            <li class="p-[10px] rounded-[8px] bg-[#FEB1C766]">Business</li>
          </ul>

          <div class="w-full py-5">
            <div class="grid grid-cols-3 gap-[20px]">
              <div>
                <NuxtImg
                  class="w-full object-cover rounded-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <div>
                <NuxtImg
                  class="w-full object-cover rounded-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <div>
                <NuxtImg
                  class="w-full object-cover rounded-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
            </div>
          </div>

          <RouterLink
            to="/pricing-plan"
            type="link"
            class="w-[233.13px] justify-between flex gap-[35.25px] border-[#7D0B2B] p-[15.34px] rounded-[36.82px] bg-[#FED0DD] mt-[15px]"
          >
            <div><NuxtImg src="/icons/Union.png" alt="" /></div>
            <div class="flex gap-2">
              <NuxtImg src="/images/msgIcon.png" alt="" />
              <span
                class="text-[#320411] font-Poppins text-[16px] leading-[24px]"
                >message</span
              >
            </div>
          </RouterLink>
        </div>
        <div>
          <h1
            class="font-Poppins font-[700] text-[24px] leading-[33.3%] tracking-[-2%] text-[#54071D] mt-10 md:mt-0 mb-10"
          >
            Other People that match your interest
          </h1>

          <div class="grid xl:grid-cols-2 gap-[20px]">
            <div
              class="border-[1.5px] border-[#FB1656] rounded-[24px] py-[8px] px-[4px] bg-[#FAFAFA] relative"
            >
              <!-- Roinded Image==== -->

              <div
                class="w-[67.5px] h-[69.49px] border-[2.25px] border-[#FB1656] rounded-full absolute top-[55%] left-[50%] translate-x-[-50%] translate-y-[-50%]"
              >
                <NuxtImg
                  class="w-full h-full rounded-full object-cover"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- grid image -->
              <div
                class="grid grid-cols-3 h-[190.42px] rounded-[24px] mb-[7.3px]"
              >
                <NuxtImg
                  class="object-cover h-full rounded-tl-[24px]"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full rounded-tr-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- data? Name -->

              <div class="pt-5">
                <p
                  class="text-center font-Poppins text-[15px] lg:text-[18px] font-[700] leading-[21px] tracking-[-1.6%] text-[#454747]"
                >
                  <span>{{ data?.firstName }}</span>
                  <span class="mx-2">{{ data?.lastName }}</span>
                  <span>{{ data?.age }}</span>
                </p>
                <!-- ==============City======== -->
                <p class="text-center text-[#454747] font-[300]">
                  ${{ data?.address.state }}
                </p>
              </div>

              <!-- Like and comment  -->
              <div
                class="w-[113.25px] mx-auto flex gap-[35.25px] p-[10.23px] rounded-[24.55px] bg-[#FED0DD] mt-[15px]"
              >
                <div><NuxtImg src="/icons/Union.png" alt="" /></div>
                <div>
                  <NuxtImg src="/images/msgIcon.png" alt="" />
                </div>
              </div>
            </div>
            <div
              class="border-[1.5px] border-[#FB1656] rounded-[24px] py-[8px] px-[4px] bg-[#FAFAFA] relative"
            >
              <!-- Roinded Image==== -->

              <div
                class="w-[67.5px] h-[69.49px] border-[2.25px] border-[#FB1656] rounded-full absolute top-[55%] left-[50%] translate-x-[-50%] translate-y-[-50%]"
              >
                <NuxtImg
                  class="w-full h-full rounded-full object-cover"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- grid image -->
              <div
                class="grid grid-cols-3 h-[190.42px] rounded-[24px] mb-[7.3px]"
              >
                <NuxtImg
                  class="object-cover h-full rounded-tl-[24px]"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full rounded-tr-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- data? Name -->

              <div class="pt-5">
                <p
                  class="text-center font-Poppins text-[15px] lg:text-[18px] font-[700] leading-[21px] tracking-[-1.6%] text-[#454747]"
                >
                  <span>{{ data?.firstName }}</span>
                  <span class="mx-2">{{ data?.lastName }}</span>
                  <span>{{ data?.age }}</span>
                </p>
                <!-- ==============City======== -->
                <p class="text-center text-[#454747] font-[300]">
                  {{ data?.address.state }}
                </p>
              </div>

              <!-- Like and comment  -->
              <div
                class="w-[113.25px] mx-auto flex gap-[35.25px] p-[10.23px] rounded-[24.55px] bg-[#FED0DD] mt-[15px]"
              >
                <div><NuxtImg src="/icons/Union.png" alt="" /></div>
                <div>
                  <NuxtImg src="/images/msgIcon.png" alt="" />
                </div>
              </div>
            </div>
            <div
              class="border-[1.5px] border-[#FB1656] rounded-[24px] py-[8px] px-[4px] bg-[#FAFAFA] relative"
            >
              <!-- Roinded Image==== -->

              <div
                class="w-[67.5px] h-[69.49px] border-[2.25px] border-[#FB1656] rounded-full absolute top-[55%] left-[50%] translate-x-[-50%] translate-y-[-50%]"
              >
                <NuxtImg
                  class="w-full h-full rounded-full object-cover"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- grid image -->
              <div
                class="grid grid-cols-3 h-[190.42px] rounded-[24px] mb-[7.3px]"
              >
                <NuxtImg
                  class="object-cover h-full rounded-tl-[24px]"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full rounded-tr-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- data? Name -->

              <div class="pt-5">
                <p
                  class="text-center font-Poppins text-[15px] lg:text-[18px] font-[700] leading-[21px] tracking-[-1.6%] text-[#454747]"
                >
                  <span>{{ data?.firstName }}</span>
                  <span class="mx-2">{{ data?.lastName }}</span>
                  <span>{{ data?.age }}</span>
                </p>
                <!-- ==============City======== -->
                <p class="text-center text-[#454747] font-[300]">
                  {{ data?.address.state }}
                </p>
              </div>

              <!-- Like and comment  -->
              <div
                class="w-[113.25px] mx-auto flex gap-[35.25px] p-[10.23px] rounded-[24.55px] bg-[#FED0DD] mt-[15px]"
              >
                <div><NuxtImg src="/icons/Union.png" alt="" /></div>
                <div>
                  <NuxtImg src="/images/msgIcon.png" alt="" />
                </div>
              </div>
            </div>
            <div
              class="border-[1.5px] border-[#FB1656] rounded-[24px] py-[8px] px-[4px] bg-[#FAFAFA] relative"
            >
              <!-- Roinded Image==== -->

              <div
                class="w-[67.5px] h-[69.49px] border-[2.25px] border-[#FB1656] rounded-full absolute top-[55%] left-[50%] translate-x-[-50%] translate-y-[-50%]"
              >
                <NuxtImg
                  class="w-full h-full rounded-full object-cover"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- grid image -->
              <div
                class="grid grid-cols-3 h-[190.42px] rounded-[24px] mb-[7.3px]"
              >
                <NuxtImg
                  class="object-cover h-full rounded-tl-[24px]"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full"
                  :src="data?.image"
                  alt=""
                />
                <NuxtImg
                  class="object-cover h-full rounded-tr-[24px]"
                  :src="data?.image"
                  alt=""
                />
              </div>
              <!-- data? Name -->

              <div class="pt-5">
                <p
                  class="text-center font-Poppins text-[15px] lg:text-[18px] font-[700] leading-[21px] tracking-[-1.6%] text-[#454747]"
                >
                  <span>{{ data?.firstName }}</span>
                  <span class="mx-2">{{ data?.lastName }}</span>
                  <span>{{ data?.age }}</span>
                </p>
                <!-- ==============City======== -->
                <p class="text-center text-[#454747] font-[300]">
                  {{ data?.address.state }}
                </p>
              </div>

              <!-- Like and comment  -->
              <div
                class="w-[113.25px] mx-auto flex gap-[35.25px] p-[10.23px] rounded-[24.55px] bg-[#FED0DD] mt-[15px]"
              >
                <div><NuxtImg src="/icons/Union.png" alt="" /></div>
                <div>
                  <NuxtImg src="/images/msgIcon.png" alt="" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
