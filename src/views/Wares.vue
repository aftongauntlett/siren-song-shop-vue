<template>
  <b-container>
    <Header />
    <div class="pt-5">
      <div class="blurb-section pb-5">
        We strive to live consciously and be divrincipled in all of our actions.
        Every item we offer is chosen with care. Our goal is to be zero waste,
        and to source all of our wares ethically. All items are vegan/cruelty
        free, and fair trade when it’s an option.
      </div>
      <div class="blurb-section">
        Send us an email using the button below if you are interested in
        purchasing an item. Please mention the item you are interested in and we
        will be in touch about availability!
      </div>

      <div
        class="sparkle-container m-3 mx-auto"
        @mouseover="showSparkles = true"
        @mouseout="showSparkles = false"
      >
        <Sparkles
          v-show="showSparkles"
          v-for="sparkle in sparkleCount"
          :key="sparkle"
          :id="sparkle"
        />
        <b-button
          type="button"
          class="main-button btn btn-outline-primary px-4 m-4"
          href="mailto:livefreewithme@protonmail.com"
          variant="link"
        >
          Email Us
        </b-button>
        <div></div>
      </div>

      <WareModal v-for="item in items" :key="item.name" :item="item" />

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
import WareModal from "../components/WareModal.vue";
import Sparkles from "../components/Sparkles.vue";
export default {
  components: { Ware, WareModal, Header, Sparkles },
  data() {
    return {
      sparkleCount: 15,
      showSparkles: false,
      items: [
        {
          image: "spiritcatcher-2.jpg",
          images: [
            require(`../assets/wares/spiritcatcher-1.jpg`),
            require(`../assets/wares/spiritcatcher-2.jpg`),
            require(`../assets/wares/spiritcatcher-3.jpg`),
            require(`../assets/wares/spiritcatcher-4.jpg`),
            require(`../assets/wares/spiritcatcher-5.jpg`),
          ],
          name: "Spirit Catcher Wand",
          description:
            'Grape vine core. Raw Selenite. Copper and twine wrapped. 26.5"Long. Spirit catcher is 6"Diameter. (Special Caution recommended.)',
          credit:
            '<ul class="description px-5 pt-3"><li>Ethically sourced or gifted by nature.</li><li>Crafted at night and cleansed under the July Buck Moon, guided byGoddess Diana.</li><li>These Wands will demand respect of the user. Use of caution in allpractices is recommended. Handcrafted by the Infinite Wizard in North Carolina, USA. 10.5" Detailedvideos on Tiktok<a href="https://www.tiktok.com/@moodalchemy/live" target="_blank">@moodalchlemy</a></div>',
          cost: "$66",
        },
        {
          image: "twilight-2.jpg",
          images: [
            require(`../assets/wares/twilight-1.jpg`),
            require(`../assets/wares/twilight-2.jpg`),
            require(`../assets/wares/twilight-3.jpg`),
            require(`../assets/wares/twilight.jpg`),
          ],
          name: "Twilight Wand",
          description:
            "Twine and sacred cannabis branches encircle raw fluorite and raw amethyst in this small but powerful wand. A spell vial sealed with wax dangles playfully as you bless and imbue with this magicians tool.",
          credit:
            '<ul class="description px-5 pt-3"><li>Ethically sourced or gifted by nature.</li><li>Crafted at night and cleansed under the July Buck Moon, guided byGoddess Diana.</li><li>These Wands will demand respect of the user. Use of caution in allpractices is recommended. Handcrafted by the Infinite Wizard in North Carolina, USA. 10.5" Detailedvideos on Tiktok<a href="https://www.tiktok.com/@moodalchemy/live" target="_blank">@moodalchlemy</a></div>',
          cost: "$125",
        },

        {
          image: "pronged-driftwood-2.jpg",
          images: [
            require(`../assets/wares/pronged-driftwood-1.jpg`),
            require(`../assets/wares/pronged-driftwood-2.jpg`),
            require(`../assets/wares/pronged-driftwood-3.jpg`),
            require(`../assets/wares/pronged-driftwood-4.jpg`),
          ],
          name: "Pronged Driftwood",
          description:
            "California driftwood with delicate shells and quartz, smokey quartz, amethyst and citrine.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$20",
        },
        {
          image: "siren-conch-1.jpg",
          images: [
            require(`../assets/wares/siren-conch-1.jpg`),
            require(`../assets/wares/siren-conch-2.jpg`),
            require(`../assets/wares/siren-conch-3.jpg`),
          ],
          name: "Siren Conch",
          description: "Majestic conch shell adorned with multiple crystals.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$20",
        },
        {
          image: "music-note-terrarium-1.jpg",
          images: [
            require(`../assets/wares/music-note-terrarium-1.jpg`),
            require(`../assets/wares/music-note-terrarium.jpg`),
          ],
          name: "Music Note Terrarium",
          description: "A bowl of magic.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$10",
        },
        {
          image: "triple-opal-necklace.jpg",
          images: [require(`../assets/wares/triple-opal-necklace.jpg`)],
          name: "Triple Opal Necklace",
          description:
            "Three beautiful opals align, copperformed by hand with a delicate crescent moon.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$86",
        },
        {
          image: "whimsey-necklace-2.jpg",
          images: [
            require(`../assets/wares/whimsey-necklace-2.jpg`),
            require(`../assets/wares/whimsey-necklace-3.jpg`),
            require(`../assets/wares/whimsey-necklace-4.jpg`),
            require(`../assets/wares/whimsey-necklace-5.jpg`),
          ],
          name: "Whimsy Necklace",
          description:
            "A very special piece. Playful moon, stars and iolite dangle from the heart of this necklace, a dazzling labradorite.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$130",
        },
        {
          image: "monet-opal-necklace.jpg",
          images: [require(`../assets/wares/monet-opal-necklace.jpg`)],
          name: "Monet Opal Heart Necklace",
          description: "Delicate beauty.",
          credit:
            'Handcrafted and copperformed in Virginia, USA. One of a kind original by <a href="https://arcaneascents.com/" target="_blank">Arcane Ascents.</a></div>',
          cost: "$75",
        },

        {
          image: "candle-quartz-2.jpg",
          images: [
            require(`../assets/wares/candle-quartz-1.jpg`),
            require(`../assets/wares/candle-quartz-2.jpg`),
            require(`../assets/wares/candle-quartz-3.jpg`),
            require(`../assets/wares/candle-quartz-4.jpg`),
          ],
          name: "Candle Quartz Driftwood",
          description:
            "A breathtaking piece designed and created by Soltive. This California driftwood wall hanging is adorned with dried flowers and quartz, with its focal point being a magnificent candle quartz pointing toward the heavens.",
          credit:
            ' One of a kind original by <a href="https://instagram.com/_soltive?utm_medium=copy_link" target="_blank">Soltive.</a></div>',
          cost: "$45",
        },
        {
          image: "cloud-necklace.jpg",
          images: [
            require(`../assets/wares/cloud-necklace-1.jpg`),
            require(`../assets/wares/cloud-necklace.jpg`),
          ],
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
.main-button {
  text-decoration: unset !important;
  z-index: 999 !important;
}

.btn {
  color: #3b5255;
  border: #3b5255 solid 1px;
  border-radius: unset;
  padding: 15px;
  font-size: 20px;
  letter-spacing: 2.5px;
}

.btn-outline-primary:hover {
  border: #00675b solid 1px !important;
  background-color: unset !important;
  color: #00675b;
}

.sparkle-container {
  position: relative;
  z-index: 999 !important;
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

.about-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}

.blurb-section {
  padding-left: 23px;
  padding-right: 23px;
  max-width: 700px;
  margin: auto;
  color: #232b2b;
  font-size: 23px;
}
</style>
