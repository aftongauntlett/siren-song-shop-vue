<template>
  <li class="d-flex flex-column">
    <b-img :src="imageLocation" class="img"></b-img>

    <b-button v-b-modal="item.name" class="modal-button"
      >See More Images</b-button
    >

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
    <div class="price-text">
      <a href="mailto:livefreewithme@protonmail.com">Contact Us</a> for
      availability and purchase.
    </div>
  </li>
</template>

<script>
export default {
  props: ["item"],
  computed: {
    imageLocation() {
      return this.item.image
        ? require(`../assets/wares/${this.item.image}`)
        : "";
    },
  },
};
</script>

<style scoped>
.modal-button {
  border-radius: unset;
}

.modal-image {
  display: block;
  margin-top: 10px;
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  box-shadow: 5px 5px 10px 5px rgba(0, 0, 0, 0.164);
}

.modal-button {
  background-color: rgb(51, 159, 167);
  font-size: 18px;
  letter-spacing: 2px;
}

.modal-button:hover {
  background-color: rgba(51, 159, 167, 0.644);
  font-size: 18px;
}

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

.price-text {
  text-align: center;
  padding-bottom: 20px;
  font-size: 20px;
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
