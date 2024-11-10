<script setup>
import { Icon } from '@iconify/vue';
import { ref, computed } from 'vue';

// Array of students with their details
const students = [
  { id: 1, imageSrc: "../public/ud.png", name: "Customer Success | How to Understant  Your Customers", rating: "4.5", reviews: "34,132", price: "$44.99", hours: "1 total hours", updateDate: "12/2017" },
  { id: 2, imageSrc: "../public/ud1.png", name: "Customer Service Success: Working with Upset Customers", rating: "4.5", reviews: "3,335", price: "$49.99", hours: "2 hours", updateDate: "3/2023" },
  { id: 3, imageSrc: "../public/ud2.png", name: "The Customer How to Manage CustomerFeedback (BITE SIZE)", rating: "4.5", reviews: "40,983", price: "$89", hours: "1 total hours", updateDate: "10/2015" },
  { id: 4, imageSrc: "../public/course1.png", name: "Customer Service Excellence- from customers to operatores", rating: "4.4", reviews: "200,300", price: "$89", hours: "4 hours", updateDate: "2/2021" },
  { id: 5, imageSrc: "../public/course2.png", name: "Marketing Basics", rating: "4.5", reviews: "180,250", price: "$89", hours: "6.5 total hours", updateDate: "2/2024" },
  { id: 6, imageSrc: "../public/students.png", name: "Data Analytics for Beginners", rating: "4.8", reviews: "300,000", price: "$89", hours: "1.5 total hours", updateDate: "4/2022" },
  { id: 7, imageSrc: "../public/students.png", name: "Customer Service Excellence", rating: "4.6", reviews: "220,500", price: "$89", hours: "3.5 total hours", updateDate: "11/2020" },
  { id: 8, imageSrc: "../public/udemyLogo.png", name: "Customer Service Training:Dealing with <br> Difficult customers", rating: "4.9", reviews: "400,000", price: "$89", hours: "6 hours", updateDate: "12/2020" },
  { id: 9, imageSrc: "../public/students.png", name: "Team Building Essentials", rating: "4.6", reviews: "50,000", price: "$89", hours: "2.5 total hour", updateDate: "1/2021" }
];

const showMore = ref(false);

const displayedStudents = computed(() => {
  return showMore.value ? students : students.slice(0, 7);
});

const toggleShowMore = () => {
  showMore.value = !showMore.value;
};
</script>

<template>
  <div class=" pl-60 mt-10 w-[62vw] font-Zeitung">
    <h1 class="text-[21pt] font-bold">Students also bought</h1>
    
    <div class="grid grid-cols-1 gap-4 w-[100%]">
      <div v-for="student in displayedStudents" :key="student.id" class="grid grid-cols-[1fr,4fr,1fr,1fr,1fr,1fr] gap-4 py-[5px] items-center w-full pb-3 border-b-[1.3px] border-gray-200">
        
        <div class="h-20 w-20">
          <img src="../public/students.png" alt="student-image" class="w-full h-full object-cover" />
        </div>
        
        <div class="font-extrabold text-[13pt]">
          <a>{{ student.name }}</a>
          <div class="flex text-gray-900 gap-1 text-[12pt]">
            <span class="text-green-900 font-extrabold">{{ student.hours }}</span>
            <span class="font-normal">Updated {{ student.updateDate }}</span>
          </div>
        </div>
        
        <div class="flex items-center gap-1">
          <span class="font-extrabold text-[12pt] text-yellow-900">{{ student.rating }}</span>
          <Icon icon="ri:star-s-fill" class="text-yellow-500" />
        </div>
        
        <div class="text-[12pt] font-normal flex items-center text-gray-700">
          <Icon icon="material-symbols:person-2-outline" width="20"/>
          {{ student.reviews }}
        </div>
        
        <div class="text-[12pt] font-normal text-gray-700">
          {{ student.price }}
        </div>
        
        <div class="flex justify-center items-center">
          <div class="border-[1.2px] border-black p-3 flex items-center justify-center h-10 w-10 rounded-full">
            <Icon icon="fluent:heart-28-regular" />
          </div>
        </div>
      </div>
    </div>
    
    <button @click="toggleShowMore" class="mt-4 border-[1.32px]  border-black w-[100%] py-3 font-bold">
      {{ showMore ? "Show Less" : "Show More" }}
    </button>
  </div>
</template>