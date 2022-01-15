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
        <b-nav-item class="pr-5" :to="{ name: 'About' }">About</b-nav-item>
        <b-nav-item class="pr-5" :to="{ name: 'Wares' }">Wares</b-nav-item>
        <b-nav-item class="pr-5" :to="{ name: 'Blog' }">Blog</b-nav-item>
        <b-nav-item class="pr-5" :to="{ name: 'Donate' }">Donate</b-nav-item>
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
  color: rgb(45, 99, 90) !important;
  border-bottom: 1px solid rgb(45, 99, 90);
}

.navbar-light .navbar-nav .nav-link {
  color: rgb(19, 179, 152);
}

.router-link-active {
  color: rgb(45, 99, 90) !important;
  border-bottom: 1px solid rgb(45, 99, 90);
}
</style>
