<script setup>
import { Icon } from "@iconify/vue";
import { ref, computed } from "vue";
</script>

<template>
  <div class="w-[56vw] ml-20 py-4 mt-10 font-Zeitung "style="padding-left: 120px;">
    <div class="flex items-center">
      <Icon icon="ri:star-s-fill" width="24" class="text-yellow-800"></Icon>
      <h1 class="text-[18pt] font-extrabold">4.5 course rating 42K ratings</h1>
    </div>
    <div class="flex items-center my-5">
      <div class="flex-grow h-px bg-slate-400"></div>
      <span class="mx-2"></span>
      <div class="flex-grow h-px bg-slate-400"></div>
    </div>
    <div>
      <div class="flex flex-wrap gap-4">
        <div
          class="h-[40vh] w-[48%] p-1 flex flex-col gap-5 border-b-[1px] border-gray-300"
        >
          <div class="flex gap-4">
            <div class="bg-black h-11 w-11 p-3 rounded-full"></div>
            <div>
              <h1 class="font-extrabold text-[13pt]">Michael W.</h1>
              <div class="flex items-center font-normal text-[11pt]">
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <span class="ml-1 font-bold text-[#747272] text-[10pt]"
                  >2 weeks ago</span
                >
              </div>
            </div>
            <div class="ml-auto">
              <Icon icon="majesticons:dots-vertical" width="25" />
            </div>
          </div>
          <div>
            <p class="pr-6 text-[13pt]">
            
              It is a good start, and a good source of 
              information to prepare yourself for the real 
              encounter that changes per every interaction.
            </p>
          </div>
          <div class="flex gap-5">
            <a href="#" class="text-[10pt] font-normal text-[#8f8e8e]"
              >Helpful?</a
            >
            <Icon icon="line-md:thumbs-up-filled" width="20"></Icon>
            <Icon icon="line-md:thumbs-down-filled" width="20"></Icon>
          </div>
        </div>

        <div
          class="h-[40vh] w-[48%] p-1 flex flex-col gap-5 border-b-[1px] border-gray-300"
        >
          <div class="flex gap-4">
            <div class="bg-black h-11 w-11 p-3 rounded-full"></div>
            <div>
              <h1 class="font-extrabold text-[13pt]">Christian B.</h1>
              <div class="flex items-center font-normal text-[11pt]">
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <span class="ml-1 font-bold text-[#747272] text-[10pt]"
                  >1 week ago</span
                >
              </div>
            </div>
            <div class="ml-auto">
              <Icon icon="majesticons:dots-vertical" width="25" />
            </div>
          </div>
          <div>
            <p class="pr-6 text-[13pt]">
             Some of the videos are photo shows and
              during those I found it diffucult to concentrate
               on the audio information.
            </p>
          </div>
          <div class="flex gap-5">
            <a href="#" class="text-[10pt] font-normal text-[#8f8e8e]"
              >Helpful?</a
            >
            <Icon icon="line-md:thumbs-up-filled" width="20"></Icon>
            <Icon icon="line-md:thumbs-down-filled" width="20"></Icon>
          </div>
        </div>

        <div class="h-[40vh] w-[48%]  flex flex-col gap-5">
          <div class="flex gap-4">
            <div class="bg-black h-11 w-11 p-3 rounded-full"></div>
            <div>
              <h1 class="font-extrabold text-[13pt]">Philippe G.</h1>
              <div class="flex items-center font-normal text-[11pt]">
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <span class="ml-1 font-bold text-[#747272] text-[10pt]"
                  >3 weeks ago</span
                >
              </div>
            </div>
            <div class="ml-auto">
              <Icon icon="majesticons:dots-vertical" width="25" />
            </div>
          </div>
          <div>
            <p class="pr-6 text-[13pt]">
              Not the first course on how to understand the
              needs of a customer but a lot of updated
              insight in relations with the new customers,
              the tools at our disposal and a fresh reminder
              how to get it done.
            </p>
          </div>
          <div class="flex gap-5">
            <a href="#" class="text-[10pt] font-normal text-[#8f8e8e]"
              >Helpful?</a
            >
            <Icon icon="line-md:thumbs-up-filled" width="20"></Icon>
            <Icon icon="line-md:thumbs-down-filled" width="20"></Icon>
          </div>
        </div>

        <div class="h-[40vh] w-[48%] p-1 flex flex-col gap-5">
          <div class="flex gap-4">
            <div class="bg-black h-11 w-11 p-3 rounded-full"></div>
            <div>
              <h1 class="font-extrabold text-[13pt]">Udemy User</h1>
              <div class="flex items-center font-normal text-[11pt]">
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <Icon icon="ri:star-s-fill" class="text-yellow-500" />
                <span class="ml-1 font-bold text-[#747272] text-[10pt]"
                  >1 month ago</span
                >
              </div>
            </div>
            <div class="ml-auto">
              <Icon icon="majesticons:dots-vertical" width="25" />
            </div>
          </div>
          <div>
            <p class="pr-6 text-[13pt]">
                How to build & satisfy team information provided is
                good.How to improve customer satisfaction is also
                useful.
            </p>
          </div>
          <div class="flex gap-5">
            <a href="#" class="text-[10pt] font-normal text-[#8f8e8e]"
              >Helpful?</a
            >
            <Icon icon="line-md:thumbs-up-filled" width="20"></Icon>
            <Icon icon="line-md:thumbs-down-filled" width="20"></Icon>
          </div>
        </div>
      </div>
    </div>
    <button class="border-[1.2px] border-black p-2 font-bold">
      Show all reviews
    </button>
  </div>
</template>