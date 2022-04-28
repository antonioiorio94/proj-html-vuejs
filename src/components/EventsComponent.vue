<template>
  <div class="container-fluid">
    <div class="container mt-5">
      <div class="row align-items-center justify-content-center mt-5">
        <div class="col-6 main-txt mb-5 mt-5">
          <h3 class="signature">Upcoming Events</h3>
          <h2>Let's Woork Togheter</h2>
        </div>
      </div>

      <!--event section-->

      <div class="row mt-5">
        <div class="col-6 g-5" v-for="event in eventList" :key="event.id">
          <div class="d-flex">
            <img :src="require(`@/assets/${event.img}`)" :alt="event.title" />
            <div class="d-flex flex-column justify-content-center mx-3">
              <p>{{ event.date }}</p>
              <h4>{{ event.title }}</h4>
              <p>
                <i class="fa-solid fa-location-dot mx-1"></i>{{ event.place }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--Newsletter section-->

    <div class="row mt-5 newsletter-section justify-content-center">
      <div class="col-3"><h3>Newsletter to get in touch</h3></div>
      <div class="col-6 text-center">
        <input class="email-input" type="text" placeholder="Your e-mail" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventsComponent",
  data() {
    return {
      eventList: [
        {
          id: 1,
          img: "artist-event-04-250x300.jpg",
          date: "NOV 22,2022",
          title: "Storytelling Workshop",
          place: "Texas, US",
        },
        {
          id: 2,
          img: "artist-event-03-250x300.jpg",
          date: "OCT 10,2022",
          title: "Painting Art Contest 2022",
          place: "New York, US",
        },
        {
          id: 3,
          img: "artist-event-02-250x300.jpg",
          date: "NOV 23,2022",
          title: "International Art Fair 2022",
          place: "Hamburg, Germany",
        },
        {
          id: 4,
          img: "artist-event-01-250x300.jpg",
          date: "DEC 15,2022",
          title: "Call For Artist 2022",
          place: "Illinois, US",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/general";
@import "@/style/component-style";

.container-fluid {
  background-image: url("@/assets/maxcoach-shape-13.png");
  background-repeat: no-repeat;
  background-position-x: right;
  h4 {
    font-weight: bold;
  }
  .newsletter-section {
    background-color: rgba(10, 10, 185, 0.545);
    background-image: url("@/assets/artist-shape-color-paint-top-left.png");
    background-repeat: no-repeat;
    padding: 50px;
    h3 {
      color: #fff;
    }
    .email-input {
      background-color: transparent;
      border-style: none;
    }
    input {
      width: 30rem;
    }
  }
  input::placeholder {
    color: #fff;
    opacity: 1;
  }
}
</style>
