<template>
  <div class="max-w-4xl mx-auto py-8 p1-64">
    <!-- Main Rating Header -->
    <div class="text-center mb-8">
      <div class="text-2xl font-semibold flex justify-center items-center">
        <span class="text-yellow-500">⭐ 4.5 course rating</span>
        <span class="ml-2 text-gray-600">• 42K ratings</span>
      </div>
    </div>

    <!-- Reviews List -->
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
      <!-- Review Card -->
      <div v-for="review in reviews" :key="review.id" class="bg-white p-6 border-t border-b border-gray-300">
        <div class="flex items-center justify-between mb-4">
          <div class="flex items-center">
            <div class="bg-gray-300 w-10 h-10 flex items-center justify-center text-white font-bold">
              {{ review.initials }}
            </div>
            <div class="ml-4">
              <h3 class="font-semibold text-gray-700">{{ review.name }}</h3>
              <p class="text-sm text-gray-500">{{ review.date }}</p>
            </div>
          </div>
          <div class="text-gray-400 text-lg">
            <!-- Three vertically aligned dots at the right end -->
            <span>⋮</span>
          </div>
        </div>
        <div class="flex items-center text-yellow-500 mb-4">
          <span v-for="star in review.stars" :key="star" class="mr-1">⭐</span>
        </div>
        <p class="text-gray-700 mb-4">{{ review.text }}</p>
        <div class="flex space-x-4 text-gray-500 text-sm">
          <span>Helpful?</span>
          <button class="flex items-center space-x-1">
            <span>👍</span>
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
          text: "It is a good start, and a good source of information to prepare yourself for the real encounter that changes per every interaction.",
        },
        {
          id: 2,
          initials: "CB",
          name: "Christina B.",
          date: "2 weeks ago",
          stars: Array(3).fill(1),
          text: "Some of the videos are photo shows and during those I found it difficult to concentrate on the audio information.",
        },
        {
          id: 3,
          initials: "PG",
          name: "Philippe G.",
          date: "3 weeks ago",
          stars: Array(4).fill(1),
          text: "Not the first course on how to understand the needs of a customer but a lot of updated insight in relations with the new customers, the tools at our disposal and a fresh reminder how to get it done.",
        },
        {
          id: 4,
          initials: "UU",
          name: "Udemy User",
          date: "1 month ago",
          stars: Array(4).fill(1),
          text: "How to build & satisfy team information provided is good. How to improve customer satisfaction is also useful.",
        },
      ],
    };
  },
};
</script>
