<script setup>
import { Icon } from "@iconify/vue";
import { ref } from 'vue';

// Toggle variable for showing full text
const showFullText = ref(false);
</script>

<template>
  <div class="w-[56vw] ml-20 py-4 mt-10 font-Zeitung flex flex-col gap-2">
    <h1 class="text-[17pt] font-extrabold">Instructor</h1>
    <div>
      <a href="" class="text-[#4c26b4] font-extrabold text-[14pt] underline">
        Laura Pickel</a
      >
      <p class="text-[13pt] text-slate-700">
        Learning Experience Designer at Lyft
      </p>
    </div>
    <div class="flex gap-5 mt-2">
      <img src="../public/profile.png" class="h-28 w-28" />
      <div class="flex flex-col gap-2 ">
        <div class="flex items-center gap-3">
            <Icon icon="ri:star-s-fill" />
          <p>4.4 Instructor Rating</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="iconamoon:certificate-badge-fill"></Icon>
          <p>54,719 Reviews</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="material-symbols:person-rounded"></Icon>
          <p>109,491 Students</p>
        </div>
        <div class="flex items-center gap-3">
          <Icon icon="material-symbols:play-circle"></Icon>
          <p>3 Courses</p>
        </div>
      </div>
    </div>
    <div>
      <em>3 parts design nerd, 4 parts passionate educator, 2 parts biker extraordinaire</em>
      <p>
        <span v-if="!showFullText">
          Laura is a Learning Experience Designer at Lyft and an Ideo U teaching team lead. In past lives, she's been a User Experience Designer at SAP, taught at the Stanford d.school, and has conducted hundreds of design thinking workshops.
        </span>
        <span v-else>
          Laura is a Learning Experience Designer at Lyft and an Ideo U teaching team lead. In past lives, she's been a User Experience Designer at SAP, taught at the Stanford d.school, and has conducted hundreds of design thinking workshops.
          <br><br>
          When she's not teaching people about using game mechanics for learning or interview techniques for empathy work, Laura can be found competing in triathlons, riding hundreds of miles on her bike for fun, or hunting for the best gluten-free bakeries around.
        </span>
      </p>
      <button @click="showFullText = !showFullText" class="text-[#4c26b4] font-bold mt-2">
        {{ showFullText ? 'See Less' : 'See More' }}
      </button>
    </div>
  </div>
</template>