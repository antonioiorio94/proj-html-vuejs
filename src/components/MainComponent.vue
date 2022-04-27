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
      <!--Immagini-->
      <div class="row mt-5">
        <div class="col-3" v-for="item in siteOption" :key="item">
          <img
            v-bind:src="require(`../assets/${item.img}`)"
            :alt="item.title"
          />
          <h4 class="mt-5">{{ item.title }}</h4>
          <p class="mt-3">{{ item.description }}</p>
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
</style>
