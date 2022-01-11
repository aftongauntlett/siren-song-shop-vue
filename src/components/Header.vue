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
      />
      <div>
        <div class="section-1 pt-5"></div>
        <div class="section-2-border">
          <div class="section-2 pt-3">{{ $route.name }}</div>
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
  font-size: 18px;
}
</style>
