<template>
  <WelcomeComponent :isButtonNeed="true" Heading="Luxury Abayas for Every Occasion!" subTitle="The Beauty of Modest Fashion..." buttonText="Shop Now"/>
  <!-- <Contact/> -->
  

  <NewProductComponent :data="dataArray"/>

  <NewsLatterComponent/>

</template>

<script setup>
import {ref} from 'vue';
import WelcomeComponent from '../components/Welcome-Component.vue'
import NewsLatterComponent from '../components/News-Letter.vue'
import NewProductComponent from '../components/NewProduct-Component.vue';

const dataArray = ref([
{img:"https://i.pinimg.com/736x/5d/5e/ca/5d5ecadf41815d9700c74fce03af5f3b.jpg",
title:'Premium Girls Abaya',
price:'$80',},

{img:"https://i.pinimg.com/736x/b3/86/ed/b386eda6d0158054c5d13865f2fe6cd3.jpg",
title:'Premium Girls Abaya',
price:'$70',},


{img:"https://i.pinimg.com/736x/c3/91/87/c3918791f4db02f00aa6371b4aba2fef.jpg",
title:'Premium Girls Abaya',
price:'$70',},

{img:"https://i.pinimg.com/736x/6d/5d/36/6d5d361ff436bfa3fc59ebdfbdb1f791.jpg",
title:'Premium Girls Abaya',
price:'$70',},

{img:"https://i.pinimg.com/736x/09/eb/4f/09eb4faea3ffa3b5365d7f22645b53e7.jpg",
title:'Premium Girls Abaya',
price:'$70',},

{img:"https://i.pinimg.com/736x/95/bb/d0/95bbd043656cf8b457251fb44a9238b9.jpg",
title:'Premium Girls Abaya',
price:'$70',},

{img:"https://i.pinimg.com/1200x/c4/53/7f/c4537f1353a25a3c22b579313a028ca8.jpg",
title:'Premium Girls Abaya',
price:'$70',},

{img:"https://i.pinimg.com/736x/eb/0c/72/eb0c72e4eb6ff4dc5fd8767b24cd5428.jpg",
title:'Premium Girls Abaya',
price:'$70',},


])
</script>