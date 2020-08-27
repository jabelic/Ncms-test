<template>
  <div id="blog">
    <Navbar />
  <li v-for="post of posts" :key="post.slug">
    <NuxtLink :to="post.slug">{{ post.title }}</NuxtLink><br>
  </li>
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
