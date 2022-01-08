<template>
  <div
    :style="`top: ${top}%; left: ${left}%; `"
    class="sparkles"
    id="example-1"
  >
    <transition name="slide-fade" v-on:leave="leave" :css="false">
      <b-icon-dot
        :style="`color: ${color}; font-size: ${size}px;`"
        v-if="show"
        :id="`sparkle-${id}`"
      >
      </b-icon-dot>
    </transition>
  </div>
</template>

<script>
import Velocity from "velocity-animate";
export default {
  props: ["id"],
  mounted: function () {
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
          translateY: `${Math.random() * 200 - 100}px`,
          translateX: `${Math.random() * 200 - 100}px`,
          opacity: 0,
        },
        { duration: 750, promiseRejectEmpty: false }
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
      colors: ["pink", "purple", "green", "rgba(26,26,26,0.5)"],
    };
  },
};
</script>

<style lang="scss">
.sparkles {
  position: absolute;
}
</style>
