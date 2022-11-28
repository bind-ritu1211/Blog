<template>
  <div>
    <div class="v-app--wrap">
      <div class="v-navbar">
        <div class="v-navbar__content">
          <div
            class="v-navbar__logo"
            style="width: 60px; height: auto; margin:18px"
          >
            <a href="/">
              <img src="~/static/img/grid.svg" class="img-fluid" alt="Blog" />
            </a>
          </div>
          <div class="spacer" />
          <div class="v-navbar__img" style="margin: 50px -14px 0px -51px;">
            <ul class="v-navbar__links-items">
              <div class="m2">
                <li>
                  <a href="/"
                    ><img
                      src="~/static/img/Vector.svg"
                      class="img-fluid"
                      alt="Blog"
                  /></a>
                </li>
                <li>
                  <a href="/"
                    ><img
                      src="~/static/img/facebook.svg"
                      class="img-fluid"
                      alt="Blog"
                  /></a>
                </li>
                <li>
                  <a href="/"
                    ><img
                      src="~/static/img/gmail.svg"
                      class="img-fluid"
                      alt="Blog"
                  /></a>
                </li>
              </div>
            </ul>
          </div>
        </div>
      </div>
      <v-content>
        <v-container>
          <nuxt />
        </v-container>
      </v-content>
    </div>
  </div>
</template>

<script>
import NavLinks from "~/data/NavLinks.json";
import Home from "~/components/Home/Intro";

export default {
  data() {
    return {
      NavData: NavLinks
    };
  },
  components: {
    home: Home
  }
};
</script>

<style>
.v-navbar {
  background-image: url("../assets/img/background-img.png");
  position: fixed;
  background: #32bdbb;
  height: 112vh;
  top: 0;
  left: 0px;
  padding-top: 20px;
}

.img-fluid {
  max-width: 100%;
  height: auto;
}

.m2 {
  width: 123px;
  height: auto;
}

.spacer {
  flex-grow: 1;
}

.v-navbar__img ul {
  list-style: none;
}

.v-navbar__img ul li {
  padding: 30px;
}

.v-navbar__img-link {
  color: #333533;
  text-decoration: none;
}

.v-navbar__img-link:hover {
  color: #ff3e81;
  transition: 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
