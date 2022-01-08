<template>
  <div
    :style="`top: ${top}%; left: ${left}%; `"
    class="sparkles"
    id="example-1"
  >
    <transition name="slide-fade" v-on:leave="leave" :css="false">
      <div
        :style="`color: ${color}; font-size: ${size}px;`"
        v-if="show"
        :id="`sparkle-${id}`"
      >
        *
      </div>
    </transition>
  </div>
</template>

<script>
import Velocity from "velocity-animate";
export default {
  props: ["id"],
  mounted: function () {
    //   Snow effect
    // setInterval(this.showSparkle, Math.random() * 7000 + 500);

    // Sparkle effect
    setInterval(this.showSparkle, Math.random() * 750 + 500);

    this.showSparkle();
  },

  methods: {
    showSparkle() {
      this.top = Math.random() * 100 - 20;
      this.left = Math.random() * 100;
      this.size = Math.random() * 60 + 30;
      this.color = this.colors[Math.floor(Math.random() * this.colors.length)];
      this.show = true;
      setTimeout(() => {
        this.show = false;
      }, 25);
    },
    leave(el, done) {
      Velocity(
        el,
        {
          // Snow Effect
          //   translateY: `${Math.random() * 1000}px`,
          //   translateX: `${Math.random() * 250}px`,

          //   Sparkle Effect
          translateY: `${Math.random() * 200 - 100}px`,
          translateX: `${Math.random() * 200 - 100}px`,

          //   Leaves Effect
          // translateY: `${Math.random() * 1000}px`,
          //   translateX: `${Math.random() * 2500}px`,

          opacity: 0,
        },
        // Snow Effect
        // { duration: 7500, promiseRejectEmpty: false }

        // Sparkle Effect
        { duration: 1250, promiseRejectEmpty: false }
      );
    },
  },

  data() {
    return {
      show: true,
      top: 0,
      left: 0,
      color: "red",
      size: 0,
      colors: ["#00675b", "#00766c", "#82ada9"],
    };
  },
};
</script>

<style lang="scss">
.sparkles {
  position: absolute;
  pointer-events: none;
}
</style>
