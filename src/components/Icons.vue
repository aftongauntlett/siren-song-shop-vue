<template>
  <b-container>
    <div class="flex-container">
      <div class="flex-item p-5">
        <b-icon icon="moon" class="icon"></b-icon>
        <div class="icon-title">ETHICALLY SOURCED</div>
        <div>
          Our goal is to be zero waste, and to source all of our wares
          ethically. All items are vegan/cruelty free, and fair trade when it’s
          an option
        </div>
      </div>

      <div class="flex-item p-5">
        <b-icon icon="star" class="icon"></b-icon>
        <div class="icon-title">VEGAN/CRUELTY FREE</div>
        <div>
          We strive to live consciously and be principled in all of our actions.
          Every item we offer is chosen with care.
        </div>
      </div>

      <div class="flex-item p-5">
        <b-icon icon="sun" class="icon"></b-icon>
        <div class="icon-title">FAIR TRADE</div>
        <div>
          We want to help uplift the collective by being a conduit of energy and
          inspiration, offering touchstones from earth and artist to humans on
          their journey.
        </div>
      </div>
    </div>
  </b-container>
</template>

<script>
export default {};
</script>

<style scoped>
.flex-container {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
  list-style: none;
}

.flex-item {
  color: rgba(12, 37, 63, 0.58);
  font-size: 18px;
  text-align: center;
  max-width: 30%;
  min-width: 350px;
}

.icon {
  font-size: 40px;
  color: #00675bc9;
}

.icon-title {
  font-size: 22px;
  padding-bottom: 15px;
  padding-top: 15px;
  letter-spacing: 2.5px;
  color: #00675bc9;
  font-weight: 600;
}
</style>
