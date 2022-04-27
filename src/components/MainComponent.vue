<template>
  <main>
    <div class="container d-flex justify-content-center flex-column">
      <div class="row align-items-center justify-content-center mt-5">
        <!--Testo-->
        <div class="col-6 main-txt">
          <h3 class="signature">Artist coaching</h3>
          <h2>I understand what it takes to create. I can help you with</h2>
        </div>
      </div>
      <!--Opzioni-->
      <div class="row mt-5">
        <div class="col-3" v-for="item in siteOption" :key="item">
          <img
            v-bind:src="require(`../assets/${item.img}`)"
            :alt="item.title"
          />
          <h4 class="mt-5">{{ item.title }}</h4>
          <p class="mt-3">{{ item.description }}</p>
        </div>
        <!--Info-->
        <div class="row mt-5">
          <div class="col- 12 col-sm-6">
            <img
              class="offset-6"
              src="@/assets/artist-quote-icon.png"
              alt="quote icon"
            />
            <h2 class="mt-5 quote">
              I coach and mentor visual artist, like you, to Create Like You
              Mean It
            </h2>
            <h3 class="signature mt-5 text-center">Martin Garrix</h3>
          </div>

          <div class="col- 12 col-sm-6 p-5">
            <p class="mt-5">
              As a coach and mentor, my ultimate goal is to motivate visual
              artists toward inspired action. I help to get you back on track to
              being the productiove,creative, meaningful and authentic artist
              you truly want to be. I support artists in craftiong and living a
              creative life as well as feeling good about themselves and thei
              art.
            </p>
            <p class="mt-5">
              As an artist and an educator for nearly 30 years, I understand
              waht it takes to create
            </p>
            <button class="mt-5">Get started today</button>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "MainComponent",
  data() {
    return {
      siteOption: [
        {
          img: "artist-box-image-01.png",
          title: "Online Courses",
          description:
            "Online art coaching now offers you a very powerful way to redisegn ypour artist mind.",
        },
        {
          img: "artist-box-image-02.png",
          title: "One to One",
          description: "Getting the necessary clarity about the current state.",
        },
        {
          img: "artist-box-image-03.png",
          title: "Anywhere",
          description:
            "Access to a valuble and portable program wich allow you to setup and live anywhere you want.",
        },
        {
          img: "artist-box-image-04.png",
          title: "On Time",
          description:
            "Punctuality is our top èpriority because it's an essential criteria ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/general";
.main-txt {
  align-items: center;
  display: flex;
  flex-direction: column;
}
.signature {
  color: $ice-cold;
  font-family: "Allura", sans-serif;
  font-size: 3rem;
  font-weight: bold;
}
h2 {
  font-size: 2rem;
  text-align: center;
  font-weight: bold;
}
h4 {
  font-weight: bold;
}
.quote {
  font-size: 5rem;
}
button {
  padding: 15px;
  border: none;
  background-color: #edd3c7;
  color: #ef6f31;
  font-weight: bold;
  border-radius: 10px;
  width: 15rem;
}
p {
  line-height: 30px;
}
</style>
