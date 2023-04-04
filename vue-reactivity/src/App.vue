<template>
  <div>
    <div class="topbar">
      <p>Cart</p>
      <Cart class="cart" :items="items" :total="total" />
    </div>
    <h1 class="ck">Cailyn's Kitchen</h1>
    <Fruit
      v-for="menu in menus"
      :key="menu"
      :img="menu.img"
      :name="menu.name"
      :price="menu.price"
      @button-clicked="add"
    />
  </div>
</template>

<script>
import Fruit from './MenuItem.vue'
import Cart from './cart.vue'

export default {
  components: {
    Fruit,
    Cart
  },
  data() {
    return {
      items: 0,
      total: 0,
      menus: [
        {
          img: 'https://www.gardeningknowhow.com/wp-content/uploads/2021/07/strawberry.jpg',
          name: 'Strawberry',
          price: 2
        },
        {
          img: 'https://billsberryfarm.com/wp-content/uploads/2020/08/blueberry-2.png',
          name: 'Blueberry',
          price: 420
        },
        {
          img: 'https://cdn.shopify.com/s/files/1/2336/3219/products/shutterstock_728062678_8992842f-1a95-4365-b326-93a367a0ab28_1024x1024.jpg?v=1569666151',
          name: 'Raspberry',
          price: 88
        },
        {
          img: 'https://cdn.shopify.com/s/files/1/2785/6868/products/43407-crystallized-citrus_blackberry_1c0e8c6c-340f-4228-9655-b659d482524c_1024x1024.jpg?v=1610743085',
          name: 'Blackberry',
          price: 999
        }
      ]
    }
  },
  methods: {
    add() {
      this.items = this.items + 1
      this.total = this.total
    }
  }
}
</script>

<style scoped>
.topbar {
  height: 100px;
  width: 100%;
  position: absolute;
  display: flex;
  top: 0px;
  left: 0px;
  background-color: rgb(81, 162, 255);
  justify-content: right;
}

.ck {
  color: white;
  margin: auto;
  position: relative;
  display: block;
  margin-top: 25px;
  text-align: center;
  font-size: 50px;
}

.cart {
  margin-top: 20px;
  margin-right: 45px;
  position: relative;
}
</style>
