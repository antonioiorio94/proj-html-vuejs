<template>
  <div class="container mt-5 mb-5">
    <div class="row">
      <div class="col-3">
        <h5>Address</h5>
        <p>
          382 NE 191st 870395 Miami, FL <br />
          support@maxcoach.com
        </p>
        <div class="col-2 d-flex align-items-center">
          <i class="fa-brands fa-twitter mx-1"></i>
          <i class="fa-brands fa-facebook-f mx-1"></i>
          <i class="fa-brands fa-instagram mx-1"></i>
          <i class="fa-brands fa-linkedin mx-1"></i>
        </div>
      </div>
      <div class="col-3">
        <h5>Explore</h5>
        <ul>
          <li>Start here</li>
          <li>Success Story</li>
          <li>Blog</li>
          <li>Courses</li>
          <li>Contact us</li>
        </ul>
      </div>
      <div class="col-3">
        <h5>Information</h5>
        <ul>
          <li>Membership</li>
          <li>Purchase guide</li>
          <li>Privacy Police</li>
          <li>Terms of services</li>
        </ul>
      </div>
      <div class="col-3">
        <h5>Instagram <span>@maxcoach</span></h5>
        <div class="d-flex">
          <img
            src="@/assets/120012142_177596140500760_8623485824101406058_n.jpg"
            alt="instagram artwork 1"
          />
          <img
            src="@/assets/120084500_197897808368764_8114555493043279565_n.jpg"
            alt="instagram artwork 2"
          />
          <img
            src="@/assets/120099363_364334431619755_7198812647386067017_n.jpg"
            alt="instagram artwork 3"
          />
        </div>
      </div>
    </div>
    <div class="row text-center mt-5">
      <p>2020 Maxcoach. All rights Reserved</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style lang="scss" scoped>
@import "@/style/general";
h5 {
  font-weight: bold;
  span {
    color: $main-orange;
    font-weight: bold;
  }
}
ul {
  list-style-type: none;
  margin: 0px;
  padding: 0px;
}
img {
  width: 8rem;
  padding: 2px;
}
</style>
