<template>
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
        class="sparkle-comp"
      />
      <div>
        <div class="section-1 pt-5">This will be</div>
        <div class="section-2-border">
          <div class="section-2 pt-3">Magical JavaScript</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Sparkles from "@/components/Sparkles";

export default {
  components: { Sparkles },
  data() {
    return {
      sparkleCount: 35,
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
