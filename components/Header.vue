<script setup>
import { Icon } from '@iconify/vue';
import { NuxtLink } from '#components';
</script>

<template>
  <header class="w-full fixed mt-5 h-max flex items-center font-Montserrat pb-5">
    <nav class="flex items-center justify-between px-7 w-full">
      <div class="flex items-center">
        <NuxtLink to="/">
          <img src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg" class="w-[100px] h-[50px]" alt="Logo" />
        </NuxtLink>
        <a class="my-3 px-3 text-[12pt] font-semiboldbold">Categories</a>
      </div>
      <div class="flex-grow mx-3 h-14 rounded-3xl border-[1px] border-black relative flex items-center bg-[rgb(243,246,249)]">
        <Icon icon="mdi:magnify" width="25" class="absolute left-4 text-gray-500"></Icon>
        <input type="text"
          class="rounded-5xl h-full w-full outline-none pl-12 text-[11pt] bg-transparent placeholder"
          placeholder="Search for anything" />
      </div>
      <div class="flex text-[12pt] font-semibold">
        <NuxtLink to="/udemy-business" class="px-3">Udemy Business</NuxtLink>
        <NuxtLink to="/teach-on-udemy" class="px-3">Teach on Udemy</NuxtLink>
        <NuxtLink to="/cart" class="px-3">
          <Icon icon="material-symbols:shopping-cart-outline-rounded" width="25"></Icon>
        </NuxtLink>
      </div>
      <div class="flex gap-2">
        <button class="px-3 border-[1.3px] h-10 w-20 text-[10pt] border-black font-extrabold">Log in</button>
        <button class="px-3 h-10 w-20 text-[10pt] text-white bg-black font-extrabold">Sign Up</button>
        <button class="px-[9px] border-[1.3px] h-10 w-10 py-[9px] border-black">
          <Icon icon="solar:global-linear" width="20"></Icon>
        </button>
      </div>
    </nav>
  </header>
</template>

