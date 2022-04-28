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
        <div class="col-4 main-txt">
          <h3 class="signature">Hello, I'm Matin</h3>
          <h2>Artist Coaching And Mentoring Might Be for You</h2>
          <button class="mt-5">Get started today</button>
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
@import "@/style/component-style";
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

  button {
    padding: 15px;
    border: none;
    background-color: $main-orange;
    color: #fff;
    font-weight: bold;
    border-radius: 10px;
    width: 15rem;
  }
}
</style>
