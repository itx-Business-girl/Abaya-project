<template>
    <header class="header header-flex">
        <h1 class="logo logo-hover">House of Hayaa</h1>
        <nav>
  <router-link class="navbar-pages navbar-pages:hover"  to="/">Home</router-link>
  <router-link class="navbar-pages navbar-pages:hover" to="/shop">Shop</router-link>
   <router-link class="navbar-pages navbar-pages:hover" to="/about">About</router-link>
   <router-link class="navbar-pages navbar-pages:hover" to="/contact">Contact <i class="fa-solid fa-cart-shopping"></i></router-link>

      </nav>
</header>
</template>


<style scoped>
.header{
  background-color:rgb(14, 13, 13);
   backdrop-filter: blur(100px);
  color:#F8F9FA;
  padding: 40px;
}
.header-flex{
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.navbar-pages{
  font-size: 20px;
  font-weight: 700;
  padding: 10px;
  gap: 50px;
  color:rgb(201, 193, 193);
   text-decoration: none;
}
.navbar-pages:hover{
  color: rgb(158, 131, 58);
   font-weight: 720;
}

.logo{
  color:rgb(201, 193, 193);
  font-size: 30px;
  font-weight: 800;
  /* padding-left: 10px; */
  font-family: 'Great Vibes', cursive;
}

.logo:hover{
  color: rgb(158, 131, 58);
  /* font-size: 26px; */
  font-weight: 850;
}
@media (max-width:768px){
    .header{
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      } 
      .navbar-pages{
      margin-top: 100px;
      padding:12px;
    }


}
</style>