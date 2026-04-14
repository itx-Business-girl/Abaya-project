<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css" integrity="sha512-2SwdPD6INVrV/lHTZbO2nodKhrnDdJK9/kg2XD1r9uGqPo1cUbujc+IYdlYdEErWNu69gVcYgdxlmVmzTWnetw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <header class="header header-flex">
        <h1 class="logo logo-hover">Abaya's Collection</h1>
        <nav>
  <router-link class="navbar-pages navbar-pages:hover"  to="/">Home</router-link>
  <router-link class="navbar-pages navbar-pages:hover" to="/shop">Shop</router-link>
   <router-link class="navbar-pages navbar-pages:hover" to="/about">About</router-link>
   <router-link class="navbar-pages navbar-pages:hover" to="/contact">Contact <i class="fa-solid fa-cart-shopping"></i></router-link>

   <!-- <RouterLink  v-for="(current,index ) in navList"  :to="current.path" class="margin-10 nav-link">
           <span v-if="current.name !== 'Add Product'">{{current.name}}</span> 
           <span v-else-if="user.role == 'admin' && current.name == 'Add Product'">{{current.name}}</span>
           </RouterLink> -->
      </nav>
</header>
</template>


<script setup>

</script>

<style scoped>


</style>