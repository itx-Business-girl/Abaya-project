<template>
  <div class="pages">
  <HeaderComponent :navList="linkList" :user="user"/>
  <main>
    <RouterView />
  </main>
  <FooterCompnent/>
  </div>
</template>

<script setup>


import HeaderComponent from './components/Header-Component.vue';
import FooterCompnent from '@/components/Footer-Compnent.vue';
 
</script>

<style scoped>
 html , body{
  height: 100%;
  margin: 0%;
   overflow-x: hidden;
 }
 .pages{
  min-height: 100vh;
  display: flex;
  flex-direction: column;
 }
 main{
  flex: 1;
 }
.container{
  display: flex;
  justify-content: center;
  margin-top: 30px;
  height: 50vh;
}
.students{
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 2px solid black;
  border-radius: 20px;
  padding: 30px;
}
ul{
  padding: 10px;
  font-size: 30px;
  margin: 35px;
  font-weight:900;
  color: rgb(48, 84, 85);
}
h1{
  
  color:rgb(26, 48, 49);
  text-transform: capitalize;
}
li{
  text-transform: capitalize;
}
/* .color-blue{
  color:blue
} */
</style>