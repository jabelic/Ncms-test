<template>
  <nav class="navbar is-light" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <!--a class="navbar-item" href="https://bulma.io">
      <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
    </a-->
    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false"
     data-target="navbarBasicExample" @click="toggleMenu" v-bind:class="{'is-active': isOpen}" >
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div class="navbar-menu" id="navbarBasicExample" v-bind:class="{'is-active': isOpen}">
    <div class="navbar-start" >
      <a class="navbar-item">
        <NuxtLink to="/">Home</NuxtLink>
      </a>

      <a class="navbar-item">
        <NuxtLink to="/Aboutme">About me</NuxtLink>
      </a>

      <a class="navbar-item">
      <NuxtLink to="/blog">Blog</NuxtLink>
      </a>

    </div>

    <div class="navbar-end">

    </div>
  </div>
</nav>
</template>

<script>

export default{
  data() {
    return {
        isOpen: false
    }
  },
  methods: {
    toggleMenu () {
      this.isOpened = !this.isOpened
    },
  },
  watch: {
    '$route': function () {
      this.isOpened = false
    }
  }
}
</script>
