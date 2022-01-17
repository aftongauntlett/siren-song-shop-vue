<template>
  <div>
    <b-modal size="lg" :id="item.name" :title="item.name" :class="title">
      <div class="d-flex flex-wrap justify-content-center">
        <b-img
          class="modal-image m-2"
          v-for="image in item.images"
          :key="image.image"
          :src="image"
        ></b-img>
      </div>
      <div class="my-4 modal-description">{{ item.description }}</div>
      <div class="price-text">
        <a href="mailto:livefreewithme@protonmail.com">Contact Us</a> for
        availability and purchase.
      </div>
    </b-modal>
  </div>
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
.title {
  color: red;
}
.modal-image {
  width: 400px;
  display: block;
}

.modal-description {
  border-top: 4px solid rgba(21, 192, 164, 0.397);
  padding-top: 20px;
  text-align: center;
  font-size: 20px;
  max-width: 70%;
  margin: auto;
  font-family: "Forum", cursive;
}
.price-text {
  text-align: center;
  padding-bottom: 20px;
  font-size: 20px;
  font-family: "Forum", cursive;
}
</style>
