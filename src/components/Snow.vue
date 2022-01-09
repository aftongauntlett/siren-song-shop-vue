<template>
  <div
    :style="`top: ${top}%; left: ${left}%; `"
    class="flurries"
    id="example-1"
  >
    <transition name="slide-fade" v-on:leave="leave" :css="false">
      <div
        :style="`color: ${color}; font-size: ${size}px;`"
        v-if="show"
        :id="`snow-${id}`"
      >
        .
      </div>
    </transition>
  </div>
</template>

<script>
import Velocity from "velocity-animate";
export default {
  props: ["id"],
  mounted: function () {
    setInterval(this.showSnow, Math.random() * 1000);

    this.showSnow();
  },

  methods: {
    showSnow() {
      this.top = Math.random() * 500 - 100;
      this.left = Math.random() * 1000 - 500;
      this.size = Math.random() * 100 + 20;
      this.color = this.colors[Math.floor(Math.random() * this.colors.length)];
      this.show = true;
      setTimeout(() => {
        this.show = false;
      }, 125);
    },
    leave(el, done) {
      Velocity(
        el,
        {
          translateY: `${Math.random() * 550}px`,
          translateX: `${Math.random() * 550}px`,
          opacity: 0,
        },
        { duration: 5500, promiseRejectEmpty: false }
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
      colors: ["purple"],
    };
  },
};
</script>

<style scoped lang="scss">
.flurries {
  position: absolute;
}

// .snow-container {
//   position: relative;
//   max-width: 50%;
//   margin: auto;
// }

.snow-container > h2 {
  z-index: 1;
}

.snow {
  z-index: 0;
}
</style>
