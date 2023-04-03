<script setup>
var menu = {
  strawberry: {
    img: "https://www.gardeningknowhow.com/wp-content/uploads/2021/07/strawberry.jpg",
    name: "Strawberry",
    price: 2,
  },
  blueberry: {
    img: "https://billsberryfarm.com/wp-content/uploads/2020/08/blueberry-2.png",
    name: "Blueberry",
    price: 420,
  },
  raspberry: {
    img: "https://cdn.shopify.com/s/files/1/2336/3219/products/shutterstock_728062678_8992842f-1a95-4365-b326-93a367a0ab28_1024x1024.jpg?v=1569666151",
    name: "Raspberry",
    price: 88,
  },
  blackberry: {
    img: "https://cdn.shopify.com/s/files/1/2785/6868/products/43407-crystallized-citrus_blackberry_1c0e8c6c-340f-4228-9655-b659d482524c_1024x1024.jpg?v=1610743085",
    name: "Blackberry",
    price: 999,
}}
</script>

<template>
<div>
    <img src="{{ menu.fruit.price }}" alt="">
    <h2>{{ menu.fruit.name }}</h2>
    <p>${{ menu.fruit.price }}</p>
    <button>Add to Cart</button>
</div>
</template>

<style scoped>

</style>