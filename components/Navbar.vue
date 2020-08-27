<template>
  <nav class="navbar is-light" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <!--a class="navbar-item" href="https://bulma.io">
      <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
    </a-->
    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" >
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div class="navbar-menu">
    <div class="navbar-start">
      <a class="navbar-item">
        Home
      </a>

      <a class="navbar-item">
        About Me
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

}
</script>
