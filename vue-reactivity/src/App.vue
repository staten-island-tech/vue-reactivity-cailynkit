<<<<<<< HEAD
<template>
  <div id="app">
      <h1>Cailyn's Kitchen</h1>
      <h3 class="openCart">shopping cart ({{ cartItems }})</h3>
      <div class="cart">
        <div class="itemList">
          <Item
            @remove="removeItem(index)"
            v-for="(inCart, index) in inCart"
            :id="`${index}`"
            :key="index"
            :name="inCart.name"
            :price="`$${inCart.price}`"
            :image="inCart.image"
          />
        </div>
        <h4>{{ cartItems }} items in Cart</h4>
        <h4>subtotal: ${{ subtotal }}</h4>
      </div>
    <section class="display">
      <Card
        @add="addCart(index)"
        v-for="(item, index) in items"
        :key="index"
        :id="`${index}`"
        :name="`${item.name} `"
        :price="`$${item.price}`"
        :image="item.image"
      />
    </section>
  </div>
=======
<script setup>

</script>

<template>
  <h1>Cailyn's Kitchen</h1>
>>>>>>> parent of 6ed2215 (kms)
</template>

<script>
import Card from "./TheCard.vue";
import Item from "./TheItem.vue";

<<<<<<< HEAD
export default {
  components: {
    Card,
    Item,
  },
  data() {
    return {
      items: [
        {
          name: "Strawberry",
          price: 10,
          image:
            "https://www.gardeningknowhow.com/wp-content/uploads/2021/07/strawberry.jpg",
        },
        {
          name: "MONSTERA",
          price: 48,
          image:
            "https://cb2.scene7.com/is/image/CB2/MonsteraDeliciosaBkPt6inSHF22/$web_pdp_main_carousel_lg$/220613165919/live-monstera-6-in-black-ceramic-pot.jpg",
        },
        {
          name: "CALATHEA ORNATA PINSTRIPE",
          price: 8,
          image:
            "https://cb2.scene7.com/is/image/CB2/CalatheaOrnataWhtPot6inSHF22/$web_pdp_main_carousel_lg$/220613165947/live-calathea-ornata-pinstripe-plant-6-in-white-ceramic-pot.jpg",
        },
        {
          name: "FICUS ELASTICA RUBBER",
          price: 28,
          image:
            "https://cb2.scene7.com/is/image/CB2/FicusElstcRbbrTrBkPot6inSHF22/$web_pdp_main_carousel_lg$/220613151917/live-ficus-elastica-rubber-plant-in-matte-black-ceramic-pot-6.jpg",
        },
        {
          name: "PEPEROMIA OBTUSIFOLIA",
          price: 19,
          image:
            "https://cb2.scene7.com/is/image/CB2/PeperomiaObtsflBkPt6inSHF22/$web_pdp_main_carousel_lg$/220613165944/live-peperomia-obtusifolia-6-in-ceramic-black-pot.jpg",
        },
        {
          name: "FAUX CACTUS",
          price: 13,
          image:
            "https://cb2.scene7.com/is/image/CB2/FauxPottedCactus4p9inSHS23/$web_pdp_main_carousel_lg$/221216141021/faux-potted-cactus-plant-49.jpg",
        },
        {
          name: "FAUX SNAKE PLANT",
          price: 17,
          image:
            "https://cb2.scene7.com/is/image/CB2/FauxSnakePlantSHF20/$web_pdp_main_carousel_lg$/200618142020/faux-snake-plant.jpg",
        },
        {
          name: "WATERMELON PEPEROMIA",
          price: 33,
          image:
            "https://cb2.scene7.com/is/image/CB2/FxPttdWtrmlnPprmPlant24inSHF22/$web_pdp_main_carousel_lg$/220613151917/faux-potted-watermelon-peperomia-plant-24.jpg",
        },
        {
          name: "TRADESCANTIA ZEBRINA",
          price: 8,
          image:
            "https://cb2.scene7.com/is/image/CB2/TrdscntZbrnPlntWtPt6inSHF22/$web_pdp_main_carousel_lg$/220613165947/live-tradescantia-zebrina-inch-plant-in-white-ceramic-pot-6.jpg",
        },
        {
          name: "FAUX FERN",
          price: 11,
          image:
            "https://cb2.scene7.com/is/image/CB2/PottedFernPlantSHS22/$web_pdp_main_carousel_lg$/211221185733/faux-fern-plant-10.jpg",
        },
        {
          name: "COIN PLANT",
          price: 13,
          image:
            "https://cb2.scene7.com/is/image/CB2/PottedCoinPlantWhtPot8inSHS21/$web_pdp_main_carousel_lg$/201123143903/8-potted-coin-plant-white-pot.jpg",
        },
        {
          name: "STRING OF BANANAS",
          price: 8,
          image:
            "https://cb2.scene7.com/is/image/CB2/PottedStrngOfBnnsWtPotSHS22/$web_pdp_main_carousel_lg$/211213121028/faux-string-of-bananas-plant-21.jpg",
        },
      ],
    };
  },
  methods: {
    addCart(index) {
      this.inCart.push(this.items[index]);
      this.subtotal = this.subtotal + this.items[index].price;
      this.cartItems = this.cartItems + 1;
    },
    removeItem(index) {
      this.inCart.splice(index, 1);
      this.subtotal = this.subtotal - this.inCart[index].price;
      this.cartItems = this.cartItems - 1;
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #151515;
  margin: 0;
  padding: 0;
  background-color: #b8cdb6;
}


.display {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.openCart {
  z-index: 1;
}

.openCart:hover {
  cursor: pointer;
  text-decoration: underline;
}

.openCart:hover ~ .cart {
  display: block;
}

.cart:hover {
  display: block;
}

.cart {
  display: none;
  position: fixed;
  top: 0;
  right: 0;
  padding-top: 5rem;
  width: 22rem;
  background-color: #fff;
  z-index: 0;
  transition: 0.3s;
}
</style>

<!-- <template>
  <div id="app">
    <h1>Cailyn's Kitchen</h1>
</div>
</template>

<script>
import MenuItem from "./MenuItem.vue";

export default {
  components: {
    MenuItem,
    Cart,
  },
  data () {
    return {
      menu: [
  {
    img: "https://www.gardeningknowhow.com/wp-content/uploads/2021/07/strawberry.jpg",
    name: "Strawberry",
    price: 2,
  },
    {
    img: "https://billsberryfarm.com/wp-content/uploads/2020/08/blueberry-2.png",
    name: "Blueberry",
    price: 420,
  },
 {
    img: "https://cdn.shopify.com/s/files/1/2336/3219/products/shutterstock_728062678_8992842f-1a95-4365-b326-93a367a0ab28_1024x1024.jpg?v=1569666151",
    name: "Raspberry",
    price: 88,
  },
 {
    img: "https://cdn.shopify.com/s/files/1/2785/6868/products/43407-crystallized-citrus_blackberry_1c0e8c6c-340f-4228-9655-b659d482524c_1024x1024.jpg?v=1610743085",
    name: "Blackberry",
    price: 999,
}]}
    }
  };
</script>

<style scoped>
#app {
  background-color: black;
  width: 100%;
  height: 100%;
}
</style> -->
=======
</style>
>>>>>>> parent of 6ed2215 (kms)
