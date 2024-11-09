<template>
  <div class="bg-gray-900 text-white py-12 p-9" >
      <h2 class="text-2xl font-bold mb-8">Explore top skills and certifications</h2>
 
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-7 px-4 md:px-8 py-8 pl-5"> 
    
      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Certifications by Issuer</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[0].items" :key="item" class="hover:text-gray-400 text-base"> 
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Web Development</h3>
        <ul class="space-y-1">
          <li v-for="item in sections[1].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">IT Certifications</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[2].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Leadership</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[3].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Data Science</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[4].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Communication</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[5].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="space-y-2">
        <h3 class="text-lg font-bold text-xl">Business Analytics & Intelligence</h3> <!-- Increased text size -->
        <ul class="space-y-1">
          <li v-for="item in sections[6].items" :key="item" class="hover:text-gray-400 text-base"> <!-- Increased text size -->
            {{ item }}
          </li>
        </ul>
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
      sections: [
        {
          title: 'Certifications by Issuer',
          items: [
            'Amazon Web Services (AWS) Certifications',
            'Six Sigma Certifications',
            'Microsoft Certifications',
            'Cisco Certifications',
            'Tableau Certifications',
            'See all Certifications',
          ],
        },
        {
          title: 'Web Development',
          items: [
            'Web Development',
            'JavaScript',
            'Angular',
            'Java',
            'See all Certifications',
          ],
        },
        {
          title: 'IT Certifications',
          items: [
            'Amazon AWS',
            'AWS Certified Cloud Practitioner',
            'AZ-900: Microsoft Azure Fundamentals',
            'AWS Certified Solutions Architect - Associate',
            'Kubernetes',
          ],
        },
        {
          title: 'Leadership',
          items: [
            'Leadership',
            'Management Skills',
            'Project Management',
            'Personal Productivity',
            'Emotional Intelligence',
          ],
        },
        {
          title: 'Data Science',
          items: [
            'Data Science',
            'Python',
            'Machine Learning',
            'ChatGPT',
            'Deep Learning',
          ],
        },
        {
          title: 'Communication',
          items: [
            'Communication Skills',
            'Presentation Skills',
            'Public Speaking',
            'Writing',
            'PowerPoint',
          ],
        },
        {
          title: 'Business Analytics & Intelligence',
          items: [
            'Microsoft Excel',
            'SQL',
            'Microsoft Power BI',
            'Data Analysis',
            'Business Analysis',
          ],
        },
      ],
    };
  },
};
</script>