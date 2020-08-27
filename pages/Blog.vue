<template>
  <div id="blog">
    <Navbar />
  <li v-for="post of posts" :key="post.slug">
    <NuxtLink :to="post.slug">{{ post.title }}</NuxtLink><br>
  </li>

<div v-for="post of posts" :key="post.slug" class="tile is-ancestor">
  <NuxtLink :to="post.slug">
  <div class="card tile is-parent"">
    <div class="card-image">
      <figure class="">
        <img width=50% height=auto src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <figure class="image is-48x48">
            <img src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image">
          </figure>
        </div>
        <div class="media-content">
          <p class="title is-4"> {{ post.title }}</p>
          <!--p class="subtitle is-6">@johnsmith</p-->
        </div>
      </div>

      <div class="content">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        Phasellus nec iaculis mauris. <a>@bulmaio</a>.
        <a href="#">#css</a> <a href="#">#responsive</a>
        <br>
        <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
      </div>
    </div>
  </div>
  </NuxtLink><br>
</div>
  </div>
</template>


<script>
//import navbar from '@/components/Navbar';
export default {
  //components:{
    //'navbar': navbar,
  //},
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Noto+Serif+JP");
#blog {
/* Google fontsで導入したいfontsからfont-familyを取ってくる */
  font-family: 'Noto Serif JP', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
