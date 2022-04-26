<template>
  <div id="app">
    <HeaderComponent />
    <HeroComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import HeroComponent from "./components/HeroComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    HeroComponent,
  },
};
</script>

<style lang="scss">
@import "@/style/general";
</style>
