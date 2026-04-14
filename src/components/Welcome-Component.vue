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