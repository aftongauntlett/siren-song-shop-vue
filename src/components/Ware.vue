<template>
  <li class="d-flex flex-column">
    <b-img :src="imageLocation" class="img"></b-img>
    <div class="name p-3 pt-5">
      {{ item.name }}
    </div>

    <div class="rainbow-box"></div>
    <div class="description p-3">
      {{ item.description }}
    </div>

    <div class="description p-3" v-html="item.credit"></div>

    <div class="cost mt-auto">
      {{ item.cost }}
    </div>
  </li>
</template>

<script>
export default {
  props: ["item"],
  computed: {
    imageLocation() {
      return this.item.image
        ? require(`../assets/images/${this.item.image}`)
        : "";
    },
  },
};
</script>

<style scoped>
.img {
  max-height: auto;
  width: auto;
}

.name {
  color: rgb(25, 24, 26);
  font-weight: bold;
  font-size: 25px;
  text-align: left;
}

.description {
  color: rgb(25, 24, 26);
  font-size: 20px;
  text-align: left;
}

.credit {
  padding-top: 20px;
  text-align: center;
  color: rgb(25, 24, 26);
  font-size: 18px;
}

.cost {
  color: rgb(51, 159, 167);
  font-weight: bold;
  font-size: 40px;
  letter-spacing: 2.5px;
  text-align: center;
  padding-top: 30px;
  padding-bottom: 30px;
}

.rainbow-box {
  width: 50%;
  height: 5px;
  background: linear-gradient(
    90deg,
    rgba(63, 218, 216, 1) 40%,
    rgba(47, 201, 226, 1) 50%,
    rgba(28, 127, 238, 1) 60%,
    rgba(95, 21, 242, 1) 70%,
    rgba(186, 12, 248, 1) 80%,
    rgba(251, 7, 217, 1) 90%
  );
}
</style>
