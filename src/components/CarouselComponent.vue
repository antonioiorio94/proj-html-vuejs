<template>
  <div class="container mt-5">
    <div class="row align-items-center justify-content-center mt-5">
      <!--Testo-->
      <div class="col-6 main-txt mb-5">
        <h3 class="signature">Testimonials</h3>
        <h2>Why do people love me?</h2>
      </div>
    </div>
    <vueper-slides
      class="no-shadow"
      :visible-slides="3"
      slide-multiple
      :gap="3"
      :slide-ratio="1 / 4"
      :dragging-distance="200"
      :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }"
    >
      <vueper-slide id="card" v-for="(slide, i) in review" :key="i">
        <template #content>
          <h4>{{ slide.title }}</h4>
          <p>{{ slide.content }}</p>
          <div class="d-flex">
            <img
              class="mx-3"
              id="user_pic"
              :src="require(`@/assets/${slide.photo}`)"
              :alt="slide.title"
            />

            <div class="d-flex flex-column">
              <p class="name mt-3">{{ slide.name }}</p>

              <p>{{ slide.profession }}</p>
            </div>
          </div>
        </template>
      </vueper-slide>
    </vueper-slides>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

export default {
  name: "CarouselComponent",
  data() {
    return {
      review: [
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-01.jpg",
        },
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-02.jpg",
        },
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-03.jpg",
        },
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-04.jpg",
        },
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-03.jpg",
        },
        {
          title: "High level of efficency and scientific teaching methods",
          content:
            "I am free to learn at my own peace, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me",
          name: "Mia Hollace",
          profession: "/Freelancer",
          photo: "artist-testimonial-avatar-02.jpg",
        },
      ],
    };
  },
  components: { VueperSlides, VueperSlide },
};
</script>

<style lang="scss" scoped>
@import "@/style/component-style";
#card {
  padding: 20px;
}
.name {
  font-weight: bold;
}
#user_pic {
  width: 100px;
  border-radius: 50%;
}
</style>
