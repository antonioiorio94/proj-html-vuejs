<template>
  <div class="container-fluid">
    <div class="container mt-5">
      <div class="row align-items-center justify-content-center mt-5">
        <div class="col-6 main-txt mb-5 mt-5">
          <h3 class="signature">Articles and Tips</h3>
          <h2>Latest From The Blog</h2>
        </div>
      </div>
      <div class="row mt-5 justify-content-between">
        <div class="col-4 card gx-3" v-for="post in blogPost" :key="post.id">
          <img :src="require(`@/assets/${post.img}`)" :alt="post.title" />
          <div class="info-article">
            <p>{{ post.section }}</p>
            <h4>{{ post.title }}</h4>
            <div class="info-date d-flex justify-content-between">
              <p>
                <i class="fa-solid fa-calendar-days mx-2"></i>{{ post.date }}
              </p>
              <p><i class="fa-solid fa-eye mx-2"></i>{{ post.views }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-12 mt-5">
          <p class="text-center">
            Get into details now? <a href="#">View all post!</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogComponent",
  data() {
    return {
      blogPost: [
        {
          id: 1,
          section: "ARTIST",
          title: "Connection Between Self-Portraits and Identity",
          date: "May 15,2020",
          views: 397,
          img: "artist-blog-02-500x680.jpg",
        },
        {
          id: 2,
          section: "ARTIST",
          title: "Pocket-sized Notebooks Hold Miniature Paintings",
          date: "May 12,2020",
          views: 603,
          img: "artist-blog-01-480x356.jpg",
        },
        {
          id: 3,
          section: "ARTIST",
          title: "Brush Stokes Energize Tree in Paintings",
          date: "May 10,2020",
          views: 688,
          img: "artist-blog-03-480x356.jpeg",
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
  background-color: rgba(238, 238, 238, 0.181);
  background-image: url("@/assets/maxcoach-shape-14-1536x343.png");
  background-repeat: no-repeat;
  background-size: contain;
  .card {
    padding: 0px;
    width: 23%;
  }
  .info-article {
    padding: 20px;
    h4 {
      font-weight: bold;
    }
  }
  .info-date {
    color: $color-silver;
  }
  a {
    color: $main-orange;
    font-weight: bold;
  }
}
</style>
