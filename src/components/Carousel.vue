<template>
  <div class="pb-5">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide
        :src="require('@/assets/images/seashell_logo.png')"
      ></b-carousel-slide>

      <b-carousel-slide
        :src="require('@/assets/images/seashell_logo.png')"
      ></b-carousel-slide>

      <b-carousel-slide
        :src="require('@/assets/images/seashell_logo.png')"
      ></b-carousel-slide>

      <b-carousel-slide
        :src="require('@/assets/images/seashell_logo.png')"
        alt="Cally with rainbow reflections across her face"
      ></b-carousel-slide>

      <b-carousel-slide
        :src="require('@/assets/images/seashell_logo.png')"
      ></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>
