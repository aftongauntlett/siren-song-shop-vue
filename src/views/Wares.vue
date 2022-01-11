<template>
  <b-container>
    <Header />
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
        {
          image: "crystals.jpeg",
          name: "Candle Quartz Driftwood",
          description:
            "A breathtaking piece designed and created by Soltive. This California driftwood wall hanging is adorned with dried flowers and quartz, with its focal point being a magnificent candle quartz pointing toward the heavens.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$45",
        },
        {
          image: "crystals.jpeg",
          name: "Pronged Driftwood",
          description:
            "California driftwood with delicate shells and quartz, smokey quartz, amethyst and citrine.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$20",
        },
        {
          image: "crystals.jpeg",
          name: "Siren Conch",
          description: "Majestic conch shell adorned with multiple crystals.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$20",
        },
        {
          image: "crystals.jpeg",
          name: "Music Note Terrarium",
          description: "A bowl of magic.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$10",
        },
        {
          image: "crystals.jpeg",
          name: "Triple Opal Necklace",
          description:
            "Three beautiful opals align, copperformed by hand with a delicate crescent moon.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$86",
        },
        {
          image: "crystals.jpeg",
          name: "Whimsy Necklace",
          description:
            "A very special piece. Playful moon, stars and iolite dangle from the heart of this necklace, a dazzling labradorite.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$130",
        },
        {
          image: "crystals.jpeg",
          name: "Monet Opal Heart Necklace",
          description: "Delicate beauty.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$75",
        },
        {
          image: "crystals.jpeg",
          name: "Stormy Night Cloud Necklace",
          description:
            "Stormcloud blue lace agate with rose quartz moon with star and toggle closure.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
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

.about-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}
</style>
