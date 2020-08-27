<template>
  <div id='app'>
  <navbar />
  <div class="container">
  <hero />
  <a href="#" v-scroll-to="'#another1'"> 下</a>


<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>

  <div id="another1">到着</div>
  <br><br><br><br>

  <br><br><br><br><br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
  <br><br><br><br>
</div>
</div>
</template>

<script>
export default {
  head() {
    return {
      //script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },

};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Noto+Serif+JP");
#app {
/* Google fontsで導入したいfontsからfont-familyを取ってくる */
  font-family: 'Noto Serif JP', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
