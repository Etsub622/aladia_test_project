<template>
  <div class="bg-gray-900 text-white py-12">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-0">
      <div class="flex flex-col items-center w-full">
        <div class="flex flex-col sm:flex-row justify-between items-center w-full mb-4">
          <h1 class="text-4xl font-bold text-center sm:text-left flex-grow">
            Top companies choose Udemy Business to build in-demand career skills.
          </h1>
          <div class="flex justify-center items-center space-x-8 mt-4 sm:mt-0 flex-shrink-0"> <!-- Ensure all logos are in one row -->
            <div v-for="logo in logos" :key="logo.name" class="flex justify-center">
              <img :src="logo.src" :alt="logo.name" class="h-8" />
            </div>
          </div>
        </div>
        <div class="border-b-2 border-white w-full"></div> <!-- Added thin white line below -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logos: [
        { name: 'Nasdaq', src: 'https://via.placeholder.com/100x50' },
        { name: 'Volkswagen', src: 'https://via.placeholder.com/100x50' },
        { name: 'Box', src: 'https://via.placeholder.com/100x50' },
        { name: 'NetApp', src: 'https://via.placeholder.com/100x50' },
        { name: 'Eventbrite', src: 'https://via.placeholder.com/100x50' },
      ],
    };
  },
};
</script>