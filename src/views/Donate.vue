<template>
  <b-container class="snow-container" v-show="(showSnow = true)">
    <Snow v-show="showSnow" v-for="snow in snowCount" :key="snow" :id="snow" />
  </b-container>
</template>

<script>
import Header from "../components/Header.vue";
import Snow from "../components/Snow.vue";
export default {
  components: { Header, Snow },
  data() {
    return {
      snowCount: 3000,
      showSnow: false,
    };
  },
};
</script>

<style>
.snow-container {
  /* position: relative; */
  max-width: 100%;
  max-height: 100%;
  /* margin: auto; */
  /* z-index: 999 !important; */
}
</style>
