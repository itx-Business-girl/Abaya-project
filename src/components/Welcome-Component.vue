<template>
<div class="welcome-flex section-height background-image">
    <h1 class="welcome-heading hero-heading">{{ Heading }}</h1>
    <p class="welcome-sub-heading sub-heading">{{ subTitle }}</p> 
    <button v-if="isButtonNeed" class="hero-button hero-button:hover">{{ buttonText }}</button> 
    
</div>
</template>

<script setup>
  defineProps({
    Heading:{
        type:String,
        default:""
    },
     subTitle:{
        type:String,
        default:""
    },
     buttonText:{
        type:String,
        default:""
    },
    isButtonNeed:{
        default:false,
        type:Boolean,
    },
  })
</script>


<style scoped>
/* Welcome components */

.background-image{
  background-image: linear-gradient(rgba(0,0,0,0.7),rgba(0,0,0,0.7)), url('https://i.pinimg.com/736x/55/aa/59/55aa59f720574178e0c7fd755b150ecb.jpg');
  background-position: center;
  background-image: no-repeate;
  background-size: cover;
}

.section-height{
  height: 100vh;
}

.welcome-heading{
  color: #b3b0a9;
  font-size: 55px;
  font-weight: 900;
  margin-bottom: 18px;
}

.welcome-sub-heading{
  color:rgb(173, 131, 15);
  font-size: 35px;
  font-weight: 700;
   /* margin-top: 10px; */
   /* margin-bottom: 0px; */
}

.welcome-flex{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  /* gap: 8px; */
}
.hero-button{
   padding: 12px 28px;
  font-size: 16px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: white;
  background: transparent;
  border: 2px solid white;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.35s ease;
  margin-top: 0px;
}

.hero-button:hover{
  background: gold;
  color: black;
  border-color: gold;
  transform: translateY(-4px);
   box-shadow: 0 10px 25px rgba(212,175,55,0.6);
}


.hero-heading{
 margin-top: 80px;
}

.sub-heading{
  margin-bottom: 60px;
}


@media (max-width: 768px){
   .welcome-heading{
  color: #b3b0a9;
  font-size: 37px;
  font-weight: 900;
  margin-bottom: 18px;
  margin-left: 15px;
}
.welcome-flex{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  /* gap: 8px; */
}
.welcome-sub-heading{
  color:rgb(173, 131, 15);
  font-size: 25px;
  font-weight: 700;
  margin-bottom: 18px;
}
.hero-button{
   width: 140px;
  font-size: 12px;
  text-transform: uppercase;
  color: white;
  cursor: pointer;
  margin-bottom: 15px;
  margin-right: 250px;
}
.section-height{
  height: 67vh;
}
    }
</style>