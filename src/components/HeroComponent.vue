<template>
  <main>
    <div class="container-fluid hero d-flex justify-content-center">
      <div class="row align-items-center">
        <!--Immagini sx-->
        <div class="col-4 left-artist-img">
          <img
            id="artwork_1"
            src="@/assets/artist-hero-image-01.jpg"
            alt="artist-img"
          />
          <img
            id="artwork_2"
            src="@/assets/artist-hero-image-02.jpg"
            alt="artist-img-2"
          />
        </div>

        <!--Testo centrale-->
        <div class="col-4 hero-txt p-5">
          <h3>Hello, I'm Matin</h3>
          <h2>Artist Coaching And Mentoring Might Be for You</h2>
          <button>Get started today</button>
        </div>

        <!--Immagini dx-->
        <div class="col-4 left-artist-img">
          <img
            id="artist_photo"
            src="@/assets/artist-hero-image-04-235x300.jpg"
            alt="artist-photo"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "HeroComponent",
};
</script>

<style lang="scss" scoped>
@import "@/style/general";
.hero {
  background-image: url("@/assets/hero-img.jpg");
  height: 62rem;
  background-size: cover;
  position: relative;
  #artwork_1 {
    position: absolute;
    top: 35rem;
    left: 18rem;
    z-index: 1;
  }
  #artwork_2 {
    position: absolute;
    top: 13rem;
    left: 29rem;
  }
  #artist_photo {
    position: absolute;
    top: 20rem;
    left: 110rem;
    width: 25rem;
  }
  h3 {
    color: $ice-cold;
  }
}
</style>
