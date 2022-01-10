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
    <Button />
  </li>
</template>

<script>
import Button from "../components/Button.vue";

export default {
  components: { Button },

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
  padding-top: 100px;
  padding-bottom: 100px;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url(https://images.unsplash.com/photo-1593570609432-49aae533e98d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80);
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
