<template>
  <Header />
  <!-- <b-container class="snow-container" v-show="(showSnow = true)">
  <b-container>
    <div>
      <div class="section-1 pt-5">This will be</div>
      <div class="section-2-border">
        <div class="section-2 pt-3">Magical JavaScript</div>
      </div>
    </div>
    <Snow v-show="showSnow" v-for="snow in snowCount" :key="snow" :id="snow" />
  </b-container> -->
</template>

<script>
import Header from "../components/Header.vue";
// import Snow from "../components/Snow.vue";
export default {
  components: { Header },
  // data() {
  //   return {
  //     snowCount: 3000,
  //     showSnow: false,
  //   };
  // },
};
</script>

<style scoped>
/* .snow-container {
  max-width: 50%;
  margin: auto;
} */
</style>
