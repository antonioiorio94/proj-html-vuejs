<template>
  <div id="app">
    <header>
      <HeaderComponent />
    </header>

    <div class="hero">
      <HeroComponent />
    </div>

    <main>
      <MainComponent />
      <CarouselComponent />
      <CourseSectionComponent />
    </main>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import HeroComponent from "./components/HeroComponent.vue";
import MainComponent from "./components/MainComponent.vue";
import CarouselComponent from "./components/CarouselComponent.vue";
import CourseSectionComponent from "./components/CourseSectionComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    HeroComponent,
    MainComponent,
    CarouselComponent,
    CourseSectionComponent,
  },
};
</script>

<style lang="scss">
@import "@/style/general";
</style>
