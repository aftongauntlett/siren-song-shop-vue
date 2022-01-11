<template>
  <b-container fluid class="footer border-top">
    <div class="d-flex flex-wrap justify-content-around">
      <div></div>
      <div>
        <h2 class="footer-header pb-3">Company</h2>
        <div class="links" v-for="link in links" :key="link.name">
          <b-link :to="{ name: link.name }"> {{ link.display }}</b-link>
        </div>
      </div>
      <div>
        <b-img
          :src="require('@/assets/images/seashell_logo.png')"
          width="200"
          fluid
          alt="stack of books"
          class="image"
        >
        </b-img>
      </div>
      <div>
        <div class="contact">
          <h2 class="footer-header pb-3">Contact</h2>
          <b-link class="email-link">livefreewithme@protonmail.com</b-link>
        </div>
      </div>
    </div>
    <div></div>
    <div class="copyright">
      © Copyright 2022 - Siren Song Shop - All Rights Reserved
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
          name: "Wares",
          display: "Wares",
        },
        {
          name: "Blog",
          display: "Blog",
        },
        {
          name: "Donate",
          display: "Donate",
        },
        // {
        //   name: "Contact",
        //   display: "Contact",
        // },
      ],
    };
  },
};
</script>

<style scoped>
.image {
  padding-top: 30px;
}

.copyright {
  margin-top: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
  display: flex;
  justify-content: center;
  font-size: 25px;
  font-weight: 600;
  font-family: "Tangerine", cursive;
}

.footer-header {
  font-size: 30px;
  color: #3b5255;
  letter-spacing: 2px;
  text-align: left;
  padding-top: 30px;
  font-weight: 600;
}

.links {
  text-align: left;
  padding-bottom: 15px;
  text-transform: uppercase;
  letter-spacing: 2.5px;
  font-size: 22px;
}

.email-link {
  text-align: left;
  padding-bottom: 15px;
  letter-spacing: 2.5px;
  font-size: 22px;
}

.footer {
  background-color: #e0e7f2;
}

a {
  color: #3b5255;
}

a:hover {
  color: #3b5255a1 !important;
  border-bottom: 1px solid;
  text-decoration: none;
}
</style>
