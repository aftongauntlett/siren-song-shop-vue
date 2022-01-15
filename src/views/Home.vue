<template>
  <div>
    <div
      :style="`background-image: url(/images/swimming.jpg)`"
      class="main-image"
    >
      <div class="background-image-cover">
        <b-container class="d-flex">
          <div class="header-text mb-auto p-5 mr-auto">
            <div>Welcome to</div>
            <h2>Siren Song Shop</h2>
          </div>
        </b-container>
      </div>
    </div>
    <Icons class="pt-5 pb-5" />
    <div class="home-wares">
      <HomeWares />
    </div>

    <About />
  </div>
</template>

<script>
import About from "./About";
import Icons from "@/components/Icons";
import HomeWares from "@/components/HomeWares";
import Sparkles from "@/components/Sparkles";

export default {
  mounted() {},

  components: { About, Icons, Sparkles, HomeWares },
  data() {
    return {
      sparkleCount: 50,
      showSparkles: false,
    };
  },
};
</script>

<style scoped>
.home-wares {
  background-color: rgb(210, 230, 238);
}
.header-text {
  color: rgb(238, 244, 245);
  text-align: left;
  font-size: 2vw;
  margin-top: 200px;
  background-color: rgba(0, 0, 0, 0.123);
}

.header-text h2 {
  font-size: 8vw;
  font-family: "Tangerine", cursive;
  letter-spacing: 3px;
}

.main-image {
  min-height: 90vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.background-image-cover {
  background-color: rgba(235, 239, 243, 0.247);
  height: 100%;
  width: 100%;
  min-height: 90vh;
}
</style>
