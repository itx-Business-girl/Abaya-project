
<template>
 <NewProductComponent :data="dataArray"/>
</template>

<script setup>
  import NewProductComponent from '@/components/NewProduct-Component.vue';
  import {ref} from 'vue';
  const dataArray = ref([
{img:"https://i.pinimg.com/736x/7a/ce/85/7ace85bbd8ab4ec937bcc12b932dae83.jpg",
title:'Premium Girls Abaya',
price:'$80',},

{img:"https://i.pinimg.com/736x/e4/7d/6d/e47d6d6815243c35e3699ba7c469138b.jpg",
title:'Modern Open Abaya',
price:'$80',},

{img:"https://i.pinimg.com/736x/71/81/87/718187b8b57b8251aea52d46a7ae4305.jpg",
title:'Elegant Dubai Abaya',
price:'$80',},

{img:"https://i.pinimg.com/736x/eb/be/d3/ebbed33a67c7fd5c7b3c4b050862d12d.jpg",
title:'Luxury Pearl Abaya',
price:'$80',},

{img:"https://i.pinimg.com/1200x/d7/8f/61/d78f61194ad0ab514a3cc929e24de033.jpg",
title:'Premium Girls Abaya',
price:'$80',},

{img:"https://i.pinimg.com/736x/15/ae/31/15ae31564c41978c23063053ea87a19c.jpg",
title:'Premium Girls Abaya',
price:'$80',},
])
</script>

<style scoped>
.shop-section{
padding:60px 20px;
text-align:center;
background:#f9f9f9;
}

.shop-heading{
font-size:36px;
margin-bottom:40px;
color:#222;
}

.products-container{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:30px;
max-width:1100px;
margin:auto;
}

.product-card{
background:white;
padding:20px;
border-radius:10px;
box-shadow:0 4px 10px rgba(0,0,0,0.1);
transition:0.3s;
}

.product-card:hover{
transform:translateY(-5px);
}

.product-card img{
width:100%;
border-radius:8px;
margin-bottom:15px;
}

.product-card h3{
font-size:20px;
margin-bottom:10px;
color:#333;
}

.price{
font-size:18px;
color:#b08d57;
margin-bottom:15px;
}

.product-card button{
padding:10px 18px;
border:none;
background:#000;
color:white;
border-radius:6px;
cursor:pointer;
transition:0.3s;
}

.product-card button:hover{
background:#b08d57;
}
</style>