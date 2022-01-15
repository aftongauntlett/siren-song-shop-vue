<template>
  <b-container>
    <div
      class="sparkle-container"
      @mouseover="showSparkles = true"
      @mouseout="showSparkles = false"
    >
      <Sparkles
        v-show="showSparkles"
        v-for="sparkle in sparkleCount"
        :key="sparkle"
        :id="sparkle"
      />
      <div>
        <div class="section-1 pt-5"></div>
        <div class="section-2-border">
          <div class="section-2 pt-3">Our Wares</div>
        </div>
      </div>
    </div>

    <div class="pt-5">
      <ul class="flex-container">
        <Ware
          class="flex-item mb-5 mx-4"
          v-for="item in items"
          :key="item.name"
          :item="item"
        />
      </ul>
    </div>
    <Button class="pb-5" text="View More" link="/Wares" />
  </b-container>
</template>

<script>
import Header from "../components/Header.vue";
import Ware from "../components/Ware.vue";
import Sparkles from "../components/Sparkles.vue";
import Button from "../components/Button.vue";

export default {
  components: { Ware, Header, Sparkles, Button },
  data() {
    return {
      sparkleCount: 15,
      showSparkles: false,
      items: [
        {
          image: "crystals.jpeg",
          name: "Spirit Catcher Wand",
          description:
            'Grape vine core. Raw Selenite. Copper and twine wrapped. 26.5"Long. Spirit catcher is 6"Diameter. (Special Caution recommended.)',
          credit:
            '<ul class="description px-5 pt-3"><li>Ethically sourced or gifted by nature.</li><li>Crafted at night and cleansed under the July Buck Moon, guided byGoddess Diana.</li><li>These Wands will demand respect of the user. Use of caution in allpractices is recommended. Handcrafted by the Infinite Wizard in North Carolina, USA. 10.5" Detailedvideos on Tiktok<a href="https://www.tiktok.com/@moodalchemy/live" target="_blank">@moodalchlemy</a></div>',
          cost: "$66",
        },
        {
          image: "crystals.jpeg",
          name: "Twilight Wand",
          description:
            "Twine and sacred cannabis branches encircle raw fluorite and raw amethyst in this small but powerful wand. A spell vial sealed with wax dangles playfully as you bless and imbue with this magicians tool.",
          credit:
            '<ul class="description px-5 pt-3"><li>Ethically sourced or gifted by nature.</li><li>Crafted at night and cleansed under the July Buck Moon, guided byGoddess Diana.</li><li>These Wands will demand respect of the user. Use of caution in allpractices is recommended. Handcrafted by the Infinite Wizard in North Carolina, USA. 10.5" Detailedvideos on Tiktok<a href="https://www.tiktok.com/@moodalchemy/live" target="_blank">@moodalchlemy</a></div>',
          cost: "$125",
        },
      ],
    };
  },
};
</script>

<style scoped>
.sparkle {
  z-index: 0;
}

.sparkle-container {
  position: relative;
  max-width: 50%;
  margin: auto;
}

.sparkle-container > h2 {
  z-index: 1;
}

.section-1 {
  color: #00675bc9;
  font-size: 23px;
}

.section-2 {
  color: #00675b;
  font-size: 40px;
}

.section-2-border {
  border-bottom: 5px solid #26a69949;
  padding-bottom: 15px;
}

.section-3 {
  padding-top: 60px;
  padding-bottom: 60px;
  color: #232b2b;
  font-size: 18px;
}

.flex-container {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  padding: 23px;
  list-style: none;
}

.flex-item {
  background: unset;
  min-width: 350px;
  max-width: 475px;
  margin-top: 10px;
  box-shadow: 1px 1px 20px 10px #3b525557;
}
</style>
