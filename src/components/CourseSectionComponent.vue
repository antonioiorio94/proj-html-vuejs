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
    <section>
      <div class="row g-5">
        <div
          class="col-12 col-sm-3 card"
          v-for="course in coursesCatalogue"
          :key="course.id"
        >
          <img
            class="cover"
            v-bind:src="require(`@/assets/${course.cover}`)"
            :alt="course.name"
          />

          <div class="course-info">
            <p class="price">${{ course.price }}</p>
            <h5>{{ course.name }}</h5>
            <div class="d-flex justify-content-around">
              <p>
                <i class="fa-solid fa-sheet-plastic"></i>
                {{ course.lesson }} Lessons
              </p>
              <p>
                <i class="fa-solid fa-user"></i>
                {{ course.students }} Students
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "CourseSectionComponent",
  data() {
    return {
      coursesCatalogue: [
        {
          id: 1,
          cover: "artist-course-01-480x480.jpg",
          name: "The Acrylic Painting Academy",
          lesson: 4,
          students: 50,
          price: 18.0,
        },
        {
          id: 2,
          cover: "artist-course-02-480x480.jpg",
          name: "Drawing and Shading: Complete Course",
          lesson: 14,
          students: 50,
          price: 21.0,
        },
        {
          id: 3,
          cover: "artist-course-03-480x480.jpg",
          name: "The Color Theory for Digital Artist",
          lesson: 7,
          students: 50,
          price: 19.0,
        },
        {
          id: 4,
          cover: "artist-course-04-480x480.jpg",
          name: "Ultimate Guide to Digital Sketching for Beginner",
          lesson: 14,
          students: 50,
          price: 35.0,
        },
        {
          id: 5,
          cover: "artist-course-05-480x480.jpg",
          name: "Portrait Drawing The Smart Way",
          lesson: 2,
          students: 50,
          price: 19.0,
        },
        {
          id: 6,
          cover: "artist-course-06-480x480.jpg",
          name: "Mastering Watercolor Painting from Beginner",
          lesson: 9,
          students: 50,
          price: 19.0,
        },
        {
          id: 7,
          cover: "artist-course-07-480x480.jpg",
          name: "The Art & Science of Drawing",
          lesson: 4,
          students: 50,
          price: 25.0,
        },
        {
          id: 8,
          cover: "artist-course-08-480x480.jpg",
          name: "The Colored Pencil Drawing Course",
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
@import "@/style/general";
@import "@/style/component-style";

.card {
  border: none;
  .course-info {
    padding: 15px;
    color: $color-silver;
    .price {
      color: $main-orange;
      font-weight: bold;
    }
    h5 {
      font-weight: bold;
      color: black;
    }
  }
}
.course-info:hover {
  border: 2px solid $main-orange;
  cursor: pointer;
}
</style>
