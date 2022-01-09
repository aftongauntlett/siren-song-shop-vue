<template>
  <b-container>
    <Header />
    <div class="pt-5">
      <ul class="flex-container">
        <Ware
          class="flex-item mb-5"
          v-for="item in items"
          :key="item.name"
          :item="item"
        />
      </ul>
    </div>
  </b-container>
</template>

<script>
import Header from "../components/Header.vue";
import Ware from "../components/Ware.vue";
export default {
  components: { Ware, Header },
  data() {
    return {
      items: [
        {
          image: "crystals.jpeg",
          name: "Spirit Catcher Wand",

          description:
            'Grape vine core. Raw Selenite. Copper and twine wrapped. 26.5"Long. Spirit catcher is 6"Diameter. (Special Caution recommended.)',
          cost: "$66",
        },
        {
          image: "crystals.jpeg",
          name: "Twilight Wand",
          description:
            "Twine and sacred cannabis branches encircle raw fluorite and raw amethyst in this small but powerful wand. A spell vial sealed with wax dangles playfully as you bless and imbue with this magicians tool.",
          cost: "$125",
        },
        {
          image: "crystals.jpeg",
          name: "Candle Quartz Driftwood",
          description:
            "A breathtaking piece designed and created by Soltive. This California driftwood wall hanging is adorned with dried flowers and quartz, with its focal point being a magnificent candle quartz pointing toward the heavens.",
          cost: "$45",
        },
        {
          image: "crystals.jpeg",
          name: "Pronged Driftwood",
          description:
            "California driftwood with delicate shells and quartz, smokey quartz, amethyst and citrine. One of a kind original by Soltive.",
          cost: "$20",
        },
        {
          image: "crystals.jpeg",
          name: "Siren Conch",
          description:
            "Majestic conch shell adorned with multiple crystals. One of a kind original by Soltive.",
          cost: "$20",
        },
        {
          image: "crystals.jpeg",
          name: "Music Note Terrarium",
          description:
            "A bowl of magic. One of a kind terrarium made by Soltive.",
          cost: "$10",
        },
        {
          image: "crystals.jpeg",
          name: "Triple Opal Necklace",
          description:
            "One of a kind original by Arcane Ascents. Three beautiful opals align, copperformed by hand with a delicate crescent moon.",
          cost: "$86",
        },
        {
          image: "crystals.jpeg",
          name: "Whimsy Necklace",
          description:
            "A very special piece. Playful moon, stars and iolite dangle from the heart of this necklace, a dazzling labradorite. Handcrafted and copperformed in Virginia, USA by Arcane Ascents.",
          cost: "$86",
        },
        {
          image: "crystals.jpeg",
          name: "Monet Opal Heart Necklace",
          description:
            "Delicate beauty, a one of a kind original by Arcane Ascents.",
          cost: "$75",
        },
        {
          image: "crystals.jpeg",
          name: "Stormy Night Cloud Necklace",
          description:
            "One of a kind original by Arcane Ascents. Stormcloud blue lace agate with rose quartz moon with star and toggle closure.",
          cost: "$105",
        },
      ],
    };
  },
};
</script>

<style scoped>
.flex-container {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  padding: 25px;
  list-style: none;
}

.flex-item {
  background: unset;
  width: 500px;
  margin-top: 10px;
  box-shadow: 1px 1px 20px 10px #3b52558a;
}

.about-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}
</style>
