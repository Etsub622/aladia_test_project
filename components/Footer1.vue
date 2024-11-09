<template>
  <div class="bg-gray-900 text-white py-12">
    <div class="w-full mx-auto px-6"> <!-- Padding on both sides -->
      <!-- Full width flex container -->
      <div class="flex justify-between items-center w-full mb-6"> <!-- Added margin-bottom for spacing -->
        <!-- Text on the left with smaller font size -->
        <h1 class="text-xl sm:text-2xl font-bold text-left">
          Top companies choose Udemy Business to build in-demand career skills.
        </h1>

        <!-- Logos on the right -->
        <div class="flex justify-end items-center space-x-8">
          <div v-for="logo in logos" :key="logo.name" class="flex justify-center">
            <img :src="logo.src" :alt="logo.name" class="h-8" />
          </div>
        </div>
      </div>

      <!-- Thinner white line with added space above it -->
      <div class="border-b border-white w-full mt-4"></div> <!-- Decreased thickness -->
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
