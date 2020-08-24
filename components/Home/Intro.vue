<template>
  <div class="w">
    <div class="home-intro__wrapper-img">
      <div class="home-intro__content">
        <ul class="link">
          <li>
            <div class="header">
              <h1> Lorem Ipsum is simply dummy text of the printing</h1>
                <div class="text-justify m3">
                  <n-link :to="`/blogs/${post.id}`">{{ post.title }}</n-link>
                </div>
            </div>
          </li>
          <li>
            <div class="header">
              <h1> Lorem Ipsum is simply dummy text of the printing</h1>
                <div class="text-justify m3">
                  <p>industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                </div>
            </div>
          </li>
          <li>
            <div class="header">
              <h1> Lorem Ipsum is simply dummy text of the printing</h1>
                <div class="text-justify m3">
                  <p>industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
      return {
        posts: []
      }
    },
    async fetch() {
      this.posts = await this.$http.$get(
        'http://127.0.0.1:8000/blog/'
      )
    }
}
</script>

<style>

.home-intro__wrapper-img{
    height: 112vh;
    background-image: url("../../assets/img/61802 1.png");
    background-position: center;
}

.home-intro__content {
    text-align: center;
    position: absolute;
    top: 60%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: black;
    width: 75%;
}

.header{
    background: #C2EFEF;
    border-radius: 35px;
    margin-top: 3em;
    padding: 6px 30px 6px 30px;
}

.text-justify{
    text-align: justify;
}

.link{
    list-style: none;
}

p{
  line-height: 1.5;
}

html{
  font-family: Rouge Script;
}
</style>
