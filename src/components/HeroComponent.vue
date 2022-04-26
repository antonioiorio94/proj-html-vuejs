<template>
  <main>
    <div class="container-fluid hero">
      <div class="row">
        <!--Immagini sx-->
        <div class="col-4 left-artist-img">
          <img src="@/assets/artist-hero-image-01.jpg" alt="artist-img" />
          <img src="@/assets/artist-hero-image-02.jpg" alt="artist-img-2" />
        </div>

        <!--Testo centrale-->
        <div class="col-4 hero-txt p-5">
          <h2>Hello, I'm Matin</h2>
          <h2>Artist Coaching And Mentoring Might Be for You</h2>
          <button>Get started today</button>
        </div>

        <!--Immagini dx-->
        <div class="col-4 left-artist-img">
          <img src="@/assets/artist-hero-image-04.jpg" alt="artist-photo" />
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
}
</style>
