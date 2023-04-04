<template>
<div id="card">
  <img src="{{ menu.img }}" alt="">
  <h1>{{ menu.name }}</h1>\
  <p>${{ menu.price }}</p>
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
#card {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  color: black;
}
</style>
