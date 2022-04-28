<template>
  <div class="container mt-5">
    <div class="row align-items-center justify-content-center mt-5">
      <!--Testo-->
      <div class="col-6 main-txt mb-5">
        <h3 class="signature">Artist coaching</h3>
        <h2>Latest Online Courses</h2>
      </div>
    </div>

    <!--sezione copertine-->
    <section></section>
  </div>
</template>

<script>
export default {
  name: "CourseSectionComponent",
  data() {
    return {
      coursesCatologue: [
        {
          cover: "artist-course-01-480x480.jpg",
          name: "The Acrylic Painting Academy",
          lesson: 4,
          students: 50,
          price: 18.0,
        },
        {
          cover: "artist-course-02-480x480.jpg",
          name: "Drawing and Shading: Complete Course",
          lesson: 14,
          students: 50,
          price: 21.0,
        },
        {
          cover: "artist-course-03-480x480.jpg",
          name: "The Color Theory for Digital Artist",
          lesson: 7,
          students: 50,
          price: 19.0,
        },
        {
          cover: "artist-course-04-480x480.jpg",
          name: "Ultimate Guide to Digital Sketching for Beginner",
          lesson: 14,
          students: 50,
          price: 35.0,
        },
        {
          cover: "artist-course-05-480x480.jpg",
          name: "Portrait Drawing The Smart Way",
          lesson: 2,
          students: 50,
          price: 19.0,
        },
        {
          cover: "artist-course-06-480x480.jpg",
          name: "Mastering Watercolor Painting from Beginner",
          lesson: 9,
          students: 50,
          price: 19.0,
        },
        {
          cover: "artist-course-07-480x480.jpg",
          name: "The Art & Science of Drawing",
          lesson: 4,
          students: 50,
          price: 25.0,
        },
        {
          cover: "artist-course-08-480x480.jpg",
          name: "The COlored Pencil Drawing Course",
          lesson: 6,
          students: 50,
          price: 22.0,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/component-style";
</style>
