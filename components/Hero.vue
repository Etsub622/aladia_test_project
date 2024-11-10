<script setup>
import { Icon } from "@iconify/vue";
import Cart from "./Cart.vue";
const isScrolled = ref(false);

const handleScroll = () => {
  if (window.scrollY > 0) {
    isScrolled.value = true;
  } else {
    isScrolled.value = false;
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
    <div
    :class="{
      'fixed top-[20px]': isScrolled,
      'fixed top-[130px]': !isScrolled }"
    class="right-[250px] z-50 w-[23%] h-screen bg-white transition-all"
  >
  
    <div>
        <Cart />
    </div>
  </div>
  <div
    class=" bg-[#161515] mt-[90px] w-screen text-white flex flex-col gap- py-8 pl-72

     font-Zeitung">
    <div class="text-[14pt] font-extrabold flex items-center space-x-2 text-[#d2cff6]">
      <a href="#">Business</a>
      <Icon icon="mdi:chevron-right" width="16" class="text-white" />
      <a href="#">Management</a>
      <Icon icon="mdi:chevron-right" width="16" class="text-white" />
      <a href="#">Customor Service</a>
    </div>

    <div class="flex flex-col justify-center gap-2">
      <h1 class="text-[27pt] font-extrabold w-[50%]">The Customer: How to Understand Their<br> Needs (BITE SIZE)</h1>
      <h2 class="font-semibold w-[70%] text-[15pt]">
        Be guided on understanding the modern customer and how their needs have changed <br> over time.
      </h2>
    </div>
    <div class="flex flex-col gap-3">
      <div class="flex gap-2 items-center">
        <div class="flex items-center font-normal text-[11pt]">
              <span class="font-extrabold text-yellow-400 text-[15pt]">4.5</span>
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-400" />
            </div>
        <a href="" class="text-[#cecaff] font-extrabold text-[15pt] underline">(42,375 ratings)</a>
        <p class="text-[15t] font-extrabold">77,425 students</p>
      </div>
      <p class="text-[12pt]">Created by <a href="" class="text-[#cecaff] font-extrabold text-[10pt] underline">Learoy Tonight</a></p>
      <div class="flex space-x-2  text-[9pt] font-bold items-center">
        <Icon icon="material-symbols-light:release-alert-rounded" width="18" class="text-white" />
        <p class="text-[13pt]">Last updated 3/2016</p>
        <Icon icon="mynaui:globe" width="18" class="text-white" />
        <p class="text-[13pt]">English</p>
        <Icon icon="ic:outline-keyboard" width="18" class="text-white" />

        <p class="text-[13pt]"> English [CC], Dutch [Auto], <a href="" class="text-[#cecaff] underline">11 more</a></p>
      </div>
    </div>
  </div>
</template>