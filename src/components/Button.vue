<template>
  <div
    class="sparkle-container m-3 mx-auto"
    @mouseover="showSparkles = true"
    @mouseout="showSparkles = false"
  >
    <Sparkles
      v-show="showSparkles"
      v-for="sparkle in sparkleCount"
      :key="sparkle"
      :id="sparkle"
    />
    <b-button
      type="button"
      class="main-button btn btn-outline-primary px-4 m-4"
      :to="link"
      variant="link"
    >
      {{ text }}
    </b-button>
    <div></div>
  </div>
</template>

<script>
import Sparkles from "@/components/Sparkles";
export default {
  components: { Sparkles },
  data() {
    return {
      sparkleCount: 15,
      showSparkles: false,
    };
  },
  props: {
    text: {
      default: "",
    },
    link: {
      default: "/",
    },
  },
};
</script>

<style scoped>
.main-button {
  text-decoration: unset !important;
  z-index: 999 !important;
}

.btn {
  color: #3b5255;
  border: #3b5255 solid 1px;
  border-radius: unset;
  padding: 15px;
  font-size: 25px;
  letter-spacing: 2.5px;
}

.btn-outline-primary:hover {
  border: rgb(50, 133, 201) solid 1px !important;
  background-color: unset !important;
  color: rgb(50, 133, 201);
}

.sparkle-container {
  position: relative;
  z-index: 999 !important;
}
</style>
