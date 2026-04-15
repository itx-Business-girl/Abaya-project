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


<style scoped>
/* product-component */

.product-cart{
  padding: 15px;
  border:2px solid #ddd;
  border-radius: 10px;
  margin-top: 70px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.9);
   overflow: hidden;
   display: flex;
  flex-direction: column;
   width: 250px;
  height: 350px;
}

.products-container{
 display: flex;
 justify-content: center;
 align-items: center;
 gap: 20px;
 flex-wrap: wrap;

}

.product-img{
  width: 100%;
  border-radius: 8px;
  object-fit: cover;
   height: 250px; 
  overflow: hidden;

}
.title{
 font-size: 18px;
 font-weight: bold;
 margin-top: 10px;
}

.price{
 font-size: 16px;
 font-weight: bold;
 margin-top: 8px;
}

.product-button{
 width: 100%;
 padding: 10px 10px;
 margin-top: 10px;
 border: none;
 background-color: rgba(0,0,0,0.9);
 color: white;
 border-radius: 6px;
}

.product-button:hover{
 transform: scale(1.03);
 transition: 0.3s;
 background-color:#b08d57;
  color: black;
  border-color: rgb(39, 33, 2);
  transform: translateY(-4px);
   box-shadow: 0 10px 25px rgba(212,175,55,0.6);
}
@media (max-width: 768px){
  .product-cart{
    width: 50%;
    height: auto;
  }
  .products-container{
 display: flex;
 justify-content: center;
 align-items: center;
 gap: 20px;
 flex-wrap: wrap;

}
}
</style>
