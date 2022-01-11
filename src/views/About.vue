<template>
  <div class="about-section">
    <div>
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
        />
        <div>
          <div class="section-1 pt-5">A little bit</div>
          <div class="section-2-border">
            <div class="section-2 pt-3">About Us</div>
          </div>
        </div>
      </div>
    </div>
    <div class="section-3">
      <div class="home-text">
        Our little family run shop is inspired by the magic of nature and the
        beauty of her elements; sea and mountains, plants and stones, sky and
        cosmos, and all of the transcendental experiences that come from our
        connection with her.
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

      <div>
        <b-img
          class="about-image"
          :src="require('@/assets/images/girl-necklace.jpeg')"
          fluid
          alt=""
        ></b-img>
      </div>

      <div>
        <b-img
          class="about-image"
          :src="require('@/assets/images/mermaid-underwater.jpg')"
          fluid
          alt=""
        ></b-img>
      </div>
    </div>
    <Button text="Help Support Our Cause" link="/donate" />
  </div>
</template>

<script>
import Button from "@/components/Button";
import Header from "../components/Header.vue";
import Sparkles from "../components/Sparkles.vue";

export default {
  mounted() {},

  components: { Button, Header, Sparkles },
  data() {
    return {
      sparkleCount: 35,
      showSparkles: false,
    };
  },
};
</script>

<style scoped>
.section-1 {
  color: #00675bc9;
  font-size: 23px;
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
  font-size: 23px;
}

.about-section {
  padding: 23px;
  max-width: 700px;
  margin: auto;
}

.about-image {
  margin-top: 5vh;
  box-shadow: 1px 1px 20px 10px #3b52558a;
  width: 500px;
}

.sparkle {
  z-index: 0;
}

.sparkle-container {
  position: relative;
  max-width: 50%;
  margin: auto;
}

.sparkle-container > h2 {
  z-index: 1;
}
</style>
