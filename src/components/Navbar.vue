<template>
  <b-navbar class="potomac-nav text" sticky>
    <b-navbar-brand :to="{ name: 'Home' }">
      <b-img
        :src="require('@/assets/images/blue-flower.jpeg')"
        width="200"
        fluid
        alt="Responsive image"
        class="pb-3"
      ></b-img>
    </b-navbar-brand>

    <b-navbar-toggle target="potomac-nav"></b-navbar-toggle>
    <b-collapse id="potomac-nav" is-nav>
      <b-navbar-nav class="nav-border ml-auto">
        <b-nav-item-dropdown
          :to="{ name: 'About' }"
          class="pr-4"
          text="About"
          right
        >
          <b-dropdown-item :to="{ name: 'Values' }">
            Our Values
          </b-dropdown-item>
          <b-dropdown-item :to="{ name: 'President' }">
            Message From President
          </b-dropdown-item>
        </b-nav-item-dropdown>
        <b-nav-item class="pr-4 test" :to="{ name: 'Careers' }"
          >Careers</b-nav-item
        >
        <b-nav-item class="pr-4" :to="{ name: 'Locations' }"
          >Locations</b-nav-item
        >
        <b-nav-item class="pr-4" :to="{ name: 'Contact' }">Contact</b-nav-item>
        <b-nav-item class="pr-4" :to="{ name: 'Employee' }"
          >Employee</b-nav-item
        >
        <b-nav-item class="pr-4" :to="{ name: 'Login' }">Login</b-nav-item>
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
.potomac-nav {
  font-family: "Montserrat", sans-serif;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  font-size: 18px;
  background-color: #ffffff;
}

.b-nav-item:hover {
  color: green !important;
}

.nav-border {
  border-top: 2px solid green;
  padding-top: 15px;
}

.navbar-light .navbar-nav .nav-link {
  color: #000080;
}

.navbar-light .navbar-nav .nav-link:hover {
  color: green;
  border-bottom: 1px solid green;
}
</style>
