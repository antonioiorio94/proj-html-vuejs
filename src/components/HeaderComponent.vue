<template>
  <header>
    <nav class="navbar navbar-expand-sm navbar-light">
      <div class="container">
        <div class="row justify-content-between">
          <div class="col-2">
            <img class="navbar-brand" src="@/assets/dark-logo.png" alt="" />
          </div>
          <div class="col-5">
            <ul class="navbar-nav">
              <li v-for="item in navBarLink" :key="item" class="nav-item">
                <a href="#" class="nav-link">{{ item }}</a>
              </li>
            </ul>
          </div>
          <div class="col-2 d-flex align-items-center justify-content-end">
            <i class="fa-brands fa-twitter mx-1"></i>
            <i class="fa-brands fa-facebook-f mx-1"></i>
            <i class="fa-brands fa-instagram mx-1"></i>
            <i class="fa-brands fa-linkedin mx-1"></i>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      navBarLink: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/general";

.navbar {
  background-color: #ffff;
  .navbar-brand {
    width: 10rem;
  }
  .row {
    width: 100%;
  }
}
i {
  color: $color-silver;
}
</style>
