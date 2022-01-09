<template>
  <div>
    <div
      :style="`background-image: url(/images/mermaid-blue.jpg)`"
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
    <Icons />
    <About />
  </div>
</template>

<script>
import Sparkles from "@/components/Sparkles";
import About from "./About";
import Icons from "@/components/Icons";
export default {
  mounted() {},

  components: { Sparkles, About, Icons },
  data() {
    return {
      sparkleCount: 50,
      showSparkles: false,
    };
  },
};
</script>

<style scoped>
.header-text {
  color: rgb(221, 230, 241);
  text-align: left;
  font-size: 3vh;
  margin-top: 200px;
}

.header-text h2 {
  font-size: 12vh;
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
  background-color: rgba(12, 37, 63, 0.58);
  height: 100%;
  width: 100%;
  min-height: 90vh;
}

.sparkle-container {
  position: relative;
  max-width: 50%;
  margin: auto;
}

.sparkle-container > h2 {
  z-index: 1;
}

.sparkle {
  z-index: 0;
}
</style>
