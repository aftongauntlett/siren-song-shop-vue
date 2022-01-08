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
            <div
              class="sparkle-container"
              @mouseover="showSparkles = true"
              @mouseout="showSparkles = false"
            >
              <Sparkles
                v-show="showSparkles"
                v-for="sparkle in sparkleCount"
                :key="sparkle"
                :id="sparkle"
                class="sparkle"
              />
              <h2>Siren Song Shop</h2>
            </div>
          </div>
        </b-container>
      </div>
    </div>
    <div class="main-section">
      <div class="section-1 pt-5">Just a little bit</div>
      <div class="section-2-border">
        <div class="section-2 pt-3">About Our Life</div>
      </div>
      <div class="section-3">
        <div class="home-text">
          Our little family run shop is inspired by the magic of nature and the
          beauty of her elements; sea and mountains, plants and stones, sky and
          cosmos, and all of the transcendental experiences that come from our
          connection with her. We are further inspired by our favorite
          one-stop-shop for all things magical and inspiring: Crystal Dragon in
          Boulder, Colorado. We have brought home many a treasure from this
          wondrous little place and want to be of service to the world in a
          similar way.
        </div>
        <div class="home-text pt-4">
          Objects in the physical world can bring joy and be tools to raise our
          frequency and connect us to a higher plane. We want to help uplift the
          collective by being a conduit of energy and inspiration, offering
          touchstones from earth and artist to humans on their journey.
        </div>
        <div class="home-text pt-4">
          We strive to live consciously and be principled in all of our actions.
          Every item we offer is chosen with care. Our goal is to be zero waste,
          and to source all of our wares ethically. All items are vegan/cruelty
          free, and fair trade when it’s an option.
        </div>
      </div>
    </div>
    <div>
      <b-button
        type="button"
        class="buttons btn btn-outline-primary mb-5"
        :to="{ name: 'Donate' }"
        target="_blank"
        variant="link"
      >
        Donate to our Cause
      </b-button>

      <div
        class="about-image"
        :style="`background-image: url(/images/cally-and-gerek.jpg)`"
      ></div>
    </div>

    <!-- <b-button
        target="_blank"
        type="button"
        class="buttons btn btn-outline-primary"
        :to="{ name: 'Wares' }"
        variant="link"
      >
        View Our Wares
      </b-button> -->
  </div>
</template>

<script>
import Sparkles from "@/components/Sparkles";
export default {
  mounted() {},

  components: { Sparkles },
  data() {
    return {
      sparkleCount: 50,
      showSparkles: false,
    };
  },
};
</script>

<style>
.buttons {
  text-decoration: unset !important;
}

.sparkle {
  z-index: 0;
}

.header-text {
  color: white;
  text-align: left;
  font-size: 3vh;
  margin-top: 200px;
}

.header-text h2 {
  font-size: 12vh;
  font-family: "Tangerine", cursive;
  letter-spacing: 3px;
}

.main-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}

.main-image {
  min-height: 90vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/* .about-image {
  width: 600px;
} */

.background-image-cover {
  background-color: rgba(12, 37, 63, 0.58);
  height: 100%;
  width: 100%;
  min-height: 90vh;
}

.section-1 {
  color: #00675bc9;
  font-size: 25px;
}

.section-2 {
  color: #00675b;
  font-size: 40px;
}

.section-2-border {
  border-bottom: 5px solid #26a69949;
  padding-bottom: 15px;
}

.section-3 {
  padding-top: 60px;
  padding-bottom: 60px;
  color: #232b2b;
  font-size: 18px;
}

.home-text {
  font-size: 22px;
}

.btn {
  color: #00675b;
  border: #00675b solid 1px;
  border-radius: unset;
  padding: 15px;
  font-size: 20px;
  letter-spacing: 2.5px;
}

.btn-outline-primary:hover {
  border: #00766c solid 1px;
  background-color: #ffffff !important;
  color: #00766c;
}

.sparkle-container {
  position: relative;
}

.sparkle-container > h2 {
  z-index: 1;
}
</style>
