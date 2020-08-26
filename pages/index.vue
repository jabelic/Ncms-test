<template>
  <div id='app'>
  <navbar />
  <div class="container">
  <hero />
  <NuxtLink VueScrollTo="''#another1'" to> 下</NuxtLink>

  </div>
  <a id="another1">到着</a>
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
      //script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },

};
</script>

<style>



</style>
