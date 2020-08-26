<template>
  <div id="blog-list">
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
