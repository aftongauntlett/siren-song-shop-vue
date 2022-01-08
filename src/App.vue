<template>
  <div id="app" class="d-flex flex-column">
    <Navbar />
    <router-view />
    <Footer class="mt-auto" />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Footer from "@/components/Footer";
export default {
  components: { Navbar, Footer },
};
</script>

<style lang="scss">
#app {
  font-family: "Forum", cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  min-height: 100vh;
  color: #00675b;
  background-color: rgb(248, 249, 250);
}
</style>
