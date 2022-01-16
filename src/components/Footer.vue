<template>
  <b-container fluid class="footer border-top">
    <div class="d-flex justify-content-center">
      <b-link class="footer-logo" href="/">
        <b-img
          :src="require('@/assets/images/seashell_logo.png')"
          width="100"
          fluid
          alt="stack of books"
          class="footer-image"
        >
        </b-img>
      </b-link>
    </div>

    <div class="pt-3 footer-links">
      <div class="links" v-for="link in links" :key="link.name">
        <b-link :to="{ name: link.name }"> {{ link.display }}</b-link>
      </div>
    </div>

    <div class="copyright">
      © Copyright 2022 - Siren Song Shop - All Rights Reserved
    </div>
    <div class="gauntlet">
      Built by
      <a href="https://gauntletdesigns.com/" target="_blank"
        >Gauntlet Designs</a
      >
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
      ],
    };
  },
};
</script>

<style scoped>
.footer-links {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.footer-image {
  padding-top: 40px;
  padding-bottom: 30px;
}

.footer-logo:hover {
  padding-bottom: 0px;
  border-bottom: unset !important;
}

.copyright {
  margin-top: 15px;
  padding-bottom: 15px;
  justify-content: center;
  font-size: 30px;
  font-family: "Tangerine", cursive;
  color: rgb(161, 201, 201) !important;
}

.gauntlet {
  justify-content: center;
  font-size: 30px;
  font-family: "Tangerine", cursive;
  color: rgb(161, 201, 201) !important;
  padding-bottom: 15px;
}

.links {
  text-align: left;
  padding-bottom: 15px;
  text-transform: uppercase;
  letter-spacing: 2.5px;
  font-size: 24px;
}

.footer {
  background-color: #2f3a3a;
}

a {
  color: rgb(21, 192, 164);
}

a:hover {
  color: rgb(161, 201, 201) !important;
  border-bottom: 2px solid rgb(21, 192, 164);
  padding-bottom: 10px;
  text-decoration: none;
}
</style>
