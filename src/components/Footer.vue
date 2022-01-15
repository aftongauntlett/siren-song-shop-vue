<template>
  <b-container fluid class="footer border-top">
    <div class="d-flex justify-content-center">
      <b-link href="/">
        <b-img
          :src="require('@/assets/images/seashell_logo.png')"
          width="100"
          fluid
          alt="stack of books"
          class="footer-logo"
        >
        </b-img>
      </b-link>
    </div>

    <div class="pt-5 footer-links">
      <div class="pr-5 links" v-for="link in links" :key="link.name">
        <b-link :to="{ name: link.name }"> {{ link.display }}</b-link>
      </div>
    </div>

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
      ],
    };
  },
};
</script>

<style scoped>
.footer-links {
  display: flex;
  justify-content: center;
  /* justify-content: space-around; */
}
.footer-logo {
  padding-top: 30px;
  padding-bottom: 30px;
  border-bottom: unset !important;
}

.copyright {
  margin-top: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
  display: flex;
  justify-content: center;
  font-size: 30px;
  font-family: "Tangerine", cursive;
}

.links {
  text-align: left;
  padding-bottom: 15px;
  text-transform: uppercase;
  letter-spacing: 2.5px;
  font-size: 24px;
}

.footer {
  background-color: #e0e7f2;
}

a {
  color: rgb(19, 179, 152);
}

a:hover {
  color: rgb(45, 99, 90) !important;
  border-bottom: 1px solid rgb(45, 99, 90);
  text-decoration: none;
}
</style>
