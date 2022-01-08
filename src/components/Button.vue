<template>
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
      class="sparkle-comp"
    />
    <b-button
      type="button"
      class="main-button btn btn-outline-primary mb-5"
      :to="{ name: 'Donate' }"
      target="_blank"
      variant="link"
    >
      Donate
    </b-button>
    <div></div>
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
</template>

<script>
import Sparkles from "@/components/Sparkles";
export default {
  components: { Sparkles },
  data() {
    return {
      sparkleCount: 30,
      showSparkles: false,
    };
  },
};
</script>

<style>
.main-button {
  text-decoration: unset !important;
  z-index: 999 !important;
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
  max-width: 20%;
  margin: auto;
  z-index: 999 !important;
}
</style>
