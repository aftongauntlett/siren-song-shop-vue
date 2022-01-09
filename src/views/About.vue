<template>
  <div class="about-section">
    <Header />
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

      <div>
        <b-img
          class="about-image"
          :src="require('@/assets/images/cally-and-gerek.jpg')"
          fluid
          alt="Owners Cally and Gerek smiling"
        ></b-img>
      </div>

      <div>
        <b-img
          class="about-image"
          :src="require('@/assets/images/cally.jpg')"
          fluid
          alt="Cally with rainbow reflections across her face"
        ></b-img>
      </div>
    </div>
    <Button />
  </div>
</template>

<script>
import Button from "@/components/Button";
import Header from "../components/Header.vue";

export default {
  mounted() {},

  components: { Button, Header },
};
</script>

<style>
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

.about-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}

.about-image {
  margin-top: 5vh;
  box-shadow: 1px 1px 20px 10px #3b52558a;
  width: 500px;
  opacity: 80%;
}
</style>
