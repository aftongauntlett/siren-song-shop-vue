<template>
  <div>
    <div
      :style="`background-image: url(/images/woman-eating.jpg)`"
      class="main-image"
    >
      <div class="background-image-cover">
        <b-container class="d-flex">
          <div class="header-text mb-auto p-5 mr-auto">
            <div>Welcome to</div>
            <h2>Siren Song Shop</h2>
          </div>
        </b-container>
      </div>
    </div>
    <div class="main-section">
      <div class="section-1 pt-5">View our</div>
      <div class="section-2-border">
        <div class="section-2 pt-3">Magical Wares</div>
      </div>
      <div class="section-3">
        <div>
          Our goal is to be zero waste, and to source all of our wares
          ethically. All items are vegan/cruelty free, and fair trade when it’s
          an option
        </div>
        <div class="pt-5">
          We strive to live consciously and be principled in all of our actions.
          Every item we offer is chosen with care.
        </div>
        <div class="pt-5">
          We want to help uplift the collective by being a conduit of energy and
          inspiration, offering touchstones from earth and artist to humans on
          their journey.
        </div>
      </div>
    </div>

    <div class="pt-2">
      <b-button
        target="_blank"
        type="button"
        class="buttons btn btn-outline-primary"
        href="http://www.applebees.com/menu"
        variant="link"
      >
        View Our Wares
      </b-button>
    </div>
    <div>
      <b-button
        type="button"
        class="buttons btn btn-outline-primary mt-4 mb-5"
        href=" https://www.applebees.com/en/"
        target="_blank"
        variant="link"
      >
        Donate to our Cause
      </b-button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.buttons {
  text-decoration: unset !important;
}

.header-text {
  color: white;
  text-align: left;
  font-size: x-large;
  margin-top: 200px;
}

.header-text h2 {
  font-size: 65px;
  letter-spacing: 3px;
}

.main-section {
  padding: 20px;
  max-width: 600px;
  margin: auto;
}

.main-image {
  min-height: 90vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.background-image-cover {
  background-color: rgba(12, 37, 63, 0.58);
  height: 100%;
  width: 100%;
  min-height: 90vh;
}

.section-1 {
  color: #000080;
  font-size: 25px;
}

.section-2 {
  color: #16345b;
  font-size: 40px;
}

.section-2-border {
  border-bottom: 5px solid #00766c;
  padding-bottom: 15px;
}

.section-3 {
  padding-top: 60px;
  padding-bottom: 60px;
  color: #232b2b;
  font-size: 18px;
}

.btn {
  color: #000080;
  border: #000080 solid 1px;
  border-radius: unset;
  padding: 15px;
  font-size: 20px;
  letter-spacing: 2.5px;
}

.btn-outline-primary:hover {
  border: #00766c solid 1px;
  background-color: #ffffff !important;
  color: #00766c;
}
</style>
