<template>
  <div class="max-w-5xl mx-auto py-8">
    <!-- Section Title -->
    <h2 class="text-2xl font-semibold mb-6 "style="padding-left: 0px;">
      More Courses by <span class="text-purple-600">Learoy Tonight</span>
    </h2>

    <!-- Courses List -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <div v-for="course in courses" :key="course.id" class="text-left">
        <!-- Course Image -->
        <img :src="course.image" :alt="course.title" class="w-full h-40 object-cover rounded-md mb-3" />

        <!-- Course Title -->
        <h3 class="font-semibold text-gray-800 leading-tight">
          {{ course.title }}
        </h3>

        <!-- Author -->
        <p class="text-gray-600 text-sm">{{ course.author }}</p>

        <!-- Rating -->
        <div class="flex items-center text-yellow-500 text-sm mt-1">
          <span>{{ course.rating }}</span>
          <span class="ml-1">⭐</span>
          <span class="ml-1 text-gray-500">({{ course.reviews }})</span>
        </div>

        <!-- Course Details -->
        <p class="text-gray-500 text-sm mt-1">{{ course.details }}</p>

        <!-- Price -->
        <p class="font-semibold text-lg mt-2">{{ course.price }}</p>
      </div>
    </div>

    <!-- Report Abuse Button -->
    <div class="text-center mt-8">
  <button class="border border-black px-6 py-2 w-full text-gray-500 text-sm font-bold rounded hover:bg-gray-100">
    Report abuse
  </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      courses: [
        {
          id: 1,
          image: "https://picsum.photos/300/200?random=1",
          title: "Culture | How to Manage Team Conflict",
          author: "Learoy Tonight",
          rating: "4.4",
          reviews: "11,870",
          details: "31 total mins • 12 lectures • All Levels",
          price: "$34.99",
        },
        {
          id: 2,
          image: "https://picsum.photos/300/200?random=2",
          title: "The Customer: How to Build Customer Loyalty (BITE SIZE)",
          author: "Learoy Tonight",
          rating: "4.4",
          reviews: "7,941",
          details: "31 total mins • 12 lectures • All Levels",
          price: "$39.99",
        },
        {
          id: 3,
          image: "https://picsum.photos/300/200?random=3",
          title: "Culture | How to be a Great Coach",
          author: "Learoy Tonight",
          rating: "4.4",
          reviews: "10,225",
          details: "30 total mins • 12 lectures • All Levels",
          price: "$39.99",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Custom styles if needed */
</style>
