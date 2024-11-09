<template>
  <div class="max-w-4xl mx-auto py-8" style="padding-left: 90px;">
    <!-- Main Rating Header -->
    <div class="text-center mb-8">
      <div class="text-2xl font-semibold flex justify-center items-center">
        <span class="text-yellow-500">⭐ 4.5 course rating</span>
        <span class="ml-2 text-gray-600">• 42K ratings</span>
      </div>
    </div>

    <!-- Reviews List -->
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-12 p1-24" >
      <!-- Review Section -->
      <div v-for="review in reviews" :key="review.id">
        <div class="flex items-center mb-2">
          <div class="bg-gray-300 rounded-full w-8 h-8 flex items-center justify-center text-white font-bold">
            {{ review.initials }}
          </div>
          <div class="ml-3">
            <h3 class="font-semibold text-gray-800">{{ review.name }}</h3>
            <p class="text-sm text-gray-500">{{ review.date }}</p>
          </div>
          <div class="ml-auto cursor-pointer text-gray-400">
            <!-- Three dots icon -->
            <span>⋮</span>
          </div>
        </div>
        <div class="flex items-center text-yellow-500 mb-2">
          <span v-for="star in review.stars" :key="star" class="mr-1">⭐</span>
        </div>
        <!-- Review Text with line breaks matching the provided image -->
        <p class="text-gray-700 leading-relaxed whitespace-pre-line">{{ review.text }}</p>
        <div class="flex space-x-4 text-gray-500 text-sm mt-3">
          <button class="flex items-center space-x-1">
            <span>👍</span>
            <span>Helpful?</span>
          </button>
          <button class="flex items-center space-x-1">
            <span>👎</span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviews: [
        {
          id: 1,
          initials: "MW",
          name: "Michael W.",
          date: "2 weeks ago",
          stars: Array(4).fill(1),
          text: "It is a good start, and a good source of\ninformation to prepare yourself for the real\nencounter that changes per every interaction.",
        },
        {
          id: 2,
          initials: "CB",
          name: "Christina B.",
          date: "2 weeks ago",
          stars: Array(3).fill(1),
          text: "Some of the videos are photo shows and\nduring those I found it difficult to concentrate\non the audio information.",
        },
        {
          id: 3,
          initials: "PG",
          name: "Philippe G.",
          date: "3 weeks ago",
          stars: Array(4).fill(1),
          text: "Not the first course on how to understand the\nneeds of a customer but a lot of updated\ninsight in relations with the new customers,\nthe tools at our disposal and a fresh reminder\nhow to get it done.",
        },
        {
          id: 4,
          initials: "UU",
          name: "Udemy User",
          date: "1 month ago",
          stars: Array(4).fill(1),
          text: "How to build & satisfy team information\nprovided is good. How to improve customer\nsatisfaction is also useful.",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Custom styles if needed */
</style>
