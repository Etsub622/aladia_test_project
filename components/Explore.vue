<template>
  <div class="container mx-auto py-8 explore-related-topics" style="padding-left: 90px;">
 
    <h2 class="text-2xl font-semibold mb-4">Explore Related Topics</h2>
    <div class="topics flex space-x-2"> <!-- Flex layout with small horizontal spacing -->
      <div class="topic bg-white hover:bg-gray-200 text-gray-700 font-bold rounded-full px-4 py-2 border border-gray-700 flex items-center justify-center cursor-pointer h-12"> <!-- Darker border, added height, and fully rounded -->
        Customer Service
      </div>
      <div class="topic bg-white hover:bg-gray-200 text-gray-700 font-bold rounded-full px-4 py-2 border border-gray-700 flex items-center justify-center cursor-pointer h-12"> <!-- Darker border, added height, and fully rounded -->
        Management
      </div>
      <div class="topic bg-white hover:bg-gray-200 text-gray-700 font-bold rounded-full px-4 py-2 border border-gray-700 flex items-center justify-center cursor-pointer h-12"> <!-- Darker border, added height, and fully rounded -->
        Business
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Explore'
};
</script>