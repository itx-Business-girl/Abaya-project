<template>
<div class="products-container">
    <div class="product-cart" v-for="value in data" :key="value.id">
        <img class="product-img" :src="value.img"/>
        <h3 class="title">{{ value.title }}</h3>
        <p class="price">{{ value.price }}</p>
        <button class="product-button product-button:hover">Buy Now</button>
    </div>
</div>
</template>

<script setup>
 defineProps(['data']);
</script>