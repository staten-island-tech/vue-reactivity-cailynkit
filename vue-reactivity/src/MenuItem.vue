<template>
<div>
    <img src="{{ menu.fruit.price }}" alt="">
    <h2>{{ menu.fruit.name }}</h2>
    <p>${{ menu.fruit.price }}</p>
    <button>Add to Cart</button>
</div>
</template>

<script>
export default {
  props: {
    img: String,
    name: String,
    price: String,
  },
};
</script>

<style scoped>

</style>