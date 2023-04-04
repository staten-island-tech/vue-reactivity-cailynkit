<template>
<div>
    <img src="" alt="">
    <h1>{{name}}</h1>
    <p>${{price}}</p>
    <button @click="$emit('buttonClicked')">Add to Cart</button>
</div>
</template>

<script>
export default {
    Name: "Fruit",
    props: {
        img: String,
        name: String,
        price: String,
    },
}
</script>

<style scoped>

</style>