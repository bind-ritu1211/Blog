<template>
  <div class="contai">
    <div class="home-intro__wrapper-img">
      <div class="home-intro__content">
        <ul class="link">
          <li>
            <nuxt-link to="/description">
            <div v-for="(data,i) in posts[0]" v-bind:key="i">
              <div class="header">
                <div>
                  <!-- <a href="/" class="href__blank"> -->
                  <!-- <nuxt-link to="/description"> -->
                <h1 class="intro__header">{{data.title}}</h1>
                <div class="text-justify m3">{{data.content}}</div>
              </div>
              </div>
            </div>
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>


<script>
import axios from "axios";

export default {
  data() {
    return {
      posts: [],
    };
  },
  mounted() {
    this.$axios
      .get("http://127.0.0.1:8000/blog/")
      .then((resp) => this.posts.push(resp.data));
  },
};
</script>

<style>
.home-intro__wrapper-img{
  height: 112vh;
  background-image: url("../../assets/img/61802 1.png");
  background-position: center;
  background-attachment: fixed;

}

.home-intro__content {
  text-align: center;
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: black;
  width: 75%;
}

.header {
  background: #c2efef;
  border-radius: 35px;
  margin-top: 3em;
  padding: 6px 30px 6px 30px;
}
.m3{
  padding: 20px;
}

.href__blank{
      text-decoration: blink;
}

.intro__header{
  text-align: left;
  margin: 20px 20px 0px;
}

.text-justify {
  text-align: justify;
}

.link {
  list-style: none;
}

p {
  line-height: 1.5;
}

html {
  font-family: Rouge Script;
}
</style>
