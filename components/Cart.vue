<script setup>
import { Icon } from '@iconify/vue';
</script>

<template>
  <!-- Outer card container without padding to align with the image -->
  <div class="flex flex-col shadow-lg border border-gray-300">
    
    <div>
      <img src="../public/video.png" />
    </div>

    <!-- Inner content container with padding for layout and spacing -->
    <div class="p-8 pr-16">
      <div class="flex text-[13pt] mt-4">
        <button class="w-[50%] pb-3 border-black border-b-2 font-bold">Personal</button>
        <button class="w-[50%] pb-3 border-[#ababab] border-b-2 font-bold text-[#ababab]">Teams</button>
      </div>

      <h1 class="font-bold text-[14pt] mt-4">Subscribe to Udemy’s top <br>courses</h1>
      <p class="text-[13pt] mt-2">
        Get this course, plus 12,000+ of our top-rated <br>courses, with Personal Plan. 
        <a class="text-purple-900 font-extrabold underline">Learn more</a>
      </p>

      <button class="bg-purple-600 h-[48px] mt-6 w-full text-white font-extrabold">
        Try Personal Plan for free
      </button>

      <div class="flex flex-col items-center mt-3 text-[12pt] gap-2">
        <p>Starting at $10.00 per month after trial</p>
        <p>Cancel anytime</p>
      </div>

      <div class="flex items-center my-3">
        <div class="flex-grow border-t border-gray-300"></div>
        <span class="px-4 text-gray-500 font-semibold text-[8pt]">or</span>
        <div class="flex-grow border-t border-gray-300"></div>
      </div>

      <h1 class="font-bold text-[13pt]">$79.99</h1>
      <button class="h-[48px] mt-3 w-full border-black border-[1.3px] text-[12pt] font-extrabold">
        Add to Cart
      </button>

      <div class="flex flex-col items-center mt-3 text-[12pt] gap-2">
        <p>Starting at $10.00 per month after trial</p>
        <p>Cancel anytime</p>
      </div>

      <!-- Share, Gift, Coupon buttons -->
      <div class="flex justify-between font-bold mt-2 text-[11pt]">
        <button class="border-purple-400 border-b-2 text-[12pt]">Share</button>
        <button class="border-purple-400 border-b-2 text-[12pt]">Gift this course</button>
        <button class="border-purple-400 border-b-2 text-[12pt]">Apply Coupon</button>
      </div>

      <!-- Applied coupon section with icon -->
      <button class="relative border-dotted h-[48px] mt-3 w-full text-[#615e5e] border-black border-[1.3px] text-[10pt] text-left pl-3 pr-10 flex items-center">
        <span class="mr-5"><strong>LETSLEARNNOW</strong> is applied Udemy coupon</span>
        <Icon icon="material-symbols:close-rounded" width="25" class="ml-auto text-blue-900" />
      </button>

      <!-- Coupon input section -->
      <div class="mt-4 w-full flex items-center">
        <input class="border-black border-[1.3px] h-[42px] w-[75%] text-slate-900 p-3 text-[10pt]" placeholder="Enter Coupon" />
        <button class="bg-slate-900 w-[25%] text-[11pt] font-extrabold h-[42px] text-white">Apply</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Additional styling, if needed */
</style>
