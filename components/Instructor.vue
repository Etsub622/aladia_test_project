<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <div class="w-[56vw] ml-20 py-4 mt-9 font-Zeitung flex flex-col gap-2 pl-32">
    <h1 class="text-[18pt] font-extrabold">Instructor</h1>
    <div>
      <a href="" class="text-[#4c26b4] font-bold text-[15pt] underline">
        Learoy Tonight
      </a>
      <p class="text-[13pt] text-slate-700">
        Bite Size Learning 
      </p>
    </div>
    <div class="flex gap-5 mt-2">
      <img src="../public/Learoy.png" class="h-28 w-30 rounded-full" /> 
      <div class="flex flex-col gap-2">
        <div class="flex items-center gap-3">
          <Icon icon="ri:star-s-fill" />
          <p>4.5 Instructor Rating</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="iconamoon:certificate-badge-fill"></Icon>
          <p>110,722 Reviews</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="material-symbols:person-rounded"></Icon>
          <p>220,885 Students</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="material-symbols:play-circle"></Icon>
          <p>13 Courses</p>
        </div>
      </div>
    </div>
    <div>
      <p class="pr-6 text-[13pt]">
        Learoy believes that an investment in education is an investment in your future business. Learoy has a driving
        passion for outcomes, business return and creating engaging learning experiences.
        Learoy Tonight is essentially bite size learning, it's all about learning that little bit now and implementing those
        new skills and knowledge in the workplace tomorrow.
        Learoy isn't your typical education company. It's a forward-thinking, digital business that's leading the way.
        We've done the research and we're driving results through education. You'll see.
      </p>
    </div>
  </div>
</template>

