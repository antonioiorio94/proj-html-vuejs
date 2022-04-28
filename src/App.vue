<template>
  <div id="app">
    <header>
      <CountdownComponent />
      <HeaderComponent />
    </header>

    <div class="hero">
      <HeroComponent />
    </div>

    <main>
      <MainComponent />
      <CarouselComponent />
      <CourseSectionComponent />
      <BlogComponent />
      <EventsComponent />
    </main>

    <footer>
      <FooterComponent />
    </footer>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import HeroComponent from "./components/HeroComponent.vue";
import MainComponent from "./components/MainComponent.vue";
import CarouselComponent from "./components/CarouselComponent.vue";
import CourseSectionComponent from "./components/CourseSectionComponent.vue";
import BlogComponent from "./components/BlogComponent.vue";
import EventsComponent from "./components/EventsComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import CountdownComponent from "./components/CountdownComponent.vue";

export default {
  name: "App",
  components: {
    CountdownComponent,
    HeaderComponent,
    HeroComponent,
    MainComponent,
    CarouselComponent,
    CourseSectionComponent,
    BlogComponent,
    EventsComponent,
    FooterComponent,
  },
};
</script>

<style lang="scss">
@import "@/style/general";
@import "@/style/component-style";
</style>
