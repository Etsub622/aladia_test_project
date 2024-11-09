<template>
  <div>
    <CourseDetails />
    <Learn />
    <Explore />
    <Requirements />
    <Instructor />
    <Review />
    <MoreCourses />
    <Footer />
    <Footer2 />
    <Footer1 />
  </div>
</template>

<script>
import Learn from "@/components/Learn.vue"; 
import Explore from "@/components/Explore.vue"; 
import Requirements from "@/components/Requirements.vue";
import Instructor from "@/components/Instructor.vue";
import Review from "@/components/Review.vue";
import MoreCourses from "@/components/MoreCourses.vue";
import Footer from "@/components/Footer.vue";
import Footer2 from "@/components/Footer2.vue";
import Footer1 from "@/components/Footer1.vue";

export default {
  components: {
    Learn,
    Explore,
    Requirements,
    Instructor,
    Review,
    MoreCourses,
    Footer,
    Footer2,
    Footer1
  },
};
</script>