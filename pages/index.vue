<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import Hero from '@/components/Hero.vue';
import Header from '@/components/Header.vue';
import HeaderScroll from '@/components/HeaderScroll.vue';
import Cart from '@/components/Cart.vue';
import Bought from '@/components/Bought.vue';
import Learn from '@/components/Learn.vue';
import Explore from '@/components/Explore.vue';
import Requirements from '@/components/Requirements.vue';
import Instructor from '@/components/Instructor.vue';
import Review from '@/components/Review.vue';
import MoreCourses from '@/components/MoreCourses.vue';
import Footer1 from '@/components/Footer1.vue';
import Footer from '@/components/Footer.vue';
import Footer2 from '@/components/Footer2.vue';
import CourseContent from '@/components/CourseContent.vue';
import FrequentlyBought from '@/components/FrequentlyBought.vue';

const hasScrolled = ref(false);
const isScrolled = ref(false);

const handleScroll = () => {
  if (window.scrollY > 50) {
    hasScrolled.value = true;
  } else {
    hasScrolled.value = false;
  }

  if (window.scrollY > 0) {
    isScrolled.value = true;
  } else {
    isScrolled.value = false;
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
 
  <div class="flex flex-col">
   
    <Header v-if="!hasScrolled" />
    <HeaderScroll v-else />
    <Hero />
    <Learn />
    <Explore />
    <CourseContent />
    <Requirements />
     <Bought />
    <FrequentlyBought />
    <Instructor />
    <Review />
    <MoreCourses />
    <Footer1 />
    <Footer />
    <Footer2 />
  </div>
</template>

<style scoped>
/* Add any additional styling here */
</style>