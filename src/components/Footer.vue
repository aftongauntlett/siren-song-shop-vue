<template>
  <b-container class="bv-example-row border-top">
    <div class="d-flex flex-wrap justify-content-around">
      <div>
        <div>
          <b-img
            :src="require('@/assets/images/logo.png')"
            width="200"
            fluid
            alt="Potomac Dining Logo"
            class="image"
          >
          </b-img>
        </div>
      </div>
      <div>
        <h2 class="footer-header pb-3">Company</h2>
        <div class="links" v-for="link in links" :key="link.name">
          <b-link :to="{ name: link.name }"> {{ link.display }}</b-link>
        </div>
      </div>
      <div>
        <div class="contact">
          <h2 class="footer-header pb-3">Contact</h2>
          <div class="pb-3">13873 Park Center Road Herndon, Virginia 20171</div>
          <div>Tel: 240-752-7565</div>
          <div class="pb-3">Fax: 703-787-6550</div>
          <b-link class="email-link">info@potomacdining.com</b-link>
        </div>
      </div>
    </div>
    <div></div>
    <div class="copyright">
      © Copyright 2022 - Potomac Family Dining Group - All Rights Reserved
    </div>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          name: "About",
          display: "About",
        },
        {
          name: "Contact",
          display: "Contact",
        },
        {
          name: "Locations",
          display: "Locations",
        },
        {
          name: "Careers",
          display: "Careers",
        },
        {
          name: "Employee",
          display: "Employee Login",
        },
      ],
    };
  },
};
</script>

<style>
.border-top {
  border-top: 1px solid #ffa500 !important;
  background-color: #ffffff;
  padding-bottom: 20px;
  padding-top: 20px;
}

.image {
  padding-top: 30px;
}

.copyright {
  border-top: 1px solid #ffa500;
  margin-top: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
  display: flex;
  justify-content: center;
  font-size: 14px;
}

.footer-header {
  font-size: 20px;
  color: #000080;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  text-align: left;
  padding-top: 30px;
  font-weight: 600;
}

.contact {
  text-align: left;
  padding-bottom: 50px;
}

.links {
  text-align: left;
  padding-bottom: 15px;
  text-transform: uppercase;
  letter-spacing: 2.5px;
  font-size: 14px;
}
</style>
