<template>
  <b-navbar toggleable="lg" class="siren-nav text" sticky>
    <b-navbar-brand class="navbar-logo" :to="{ name: 'Home' }">
      <b-img
        :src="require('@/assets/images/seashell_logo.png')"
        width="100"
        fluid
        alt="Responsive image"
        class="pb-3 nav-image"
      ></b-img>
    </b-navbar-brand>

    <b-navbar-toggle target="siren-nav"></b-navbar-toggle>
    <b-collapse id="siren-nav" is-nav>
      <b-navbar-nav class="nav-border ml-auto">
        <b-nav-item class="pr-4" :to="{ name: 'About' }">About</b-nav-item>
        <b-nav-item class="pr-4" :to="{ name: 'Wares' }">Wares</b-nav-item>
        <b-nav-item class="pr-4" :to="{ name: 'Blog' }">Blog</b-nav-item>
        <b-nav-item class="pr-4" :to="{ name: 'Donate' }">Donate</b-nav-item>
        <b-nav-item class="pr-4" :to="{ name: 'Contact' }">Contact</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
.siren-nav {
  letter-spacing: 2px;
  font-size: 30px;
  background-color: #e0e7f2;
}

.navbar-logo {
  border-bottom: unset !important;
}

.navbar-light .navbar-nav .nav-link:hover {
  color: #3b5255a1 !important;
  border-bottom: 1px solid #3b5255a1;
}

.navbar-light .navbar-nav .nav-link:active {
  color: #3b5255 !important;
  border-bottom: 1px solid #3b5255;
}

.navbar-light .navbar-nav .nav-link {
  color: #3b5255;
}

.b-nav-item {
  color: #3b5255 !important;
}

.router-link-active {
  color: #3b5255 !important;
  border-bottom: 1px solid #3b5255;
}
</style>
