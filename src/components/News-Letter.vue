<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css" integrity="sha512-2SwdPD6INVrV/lHTZbO2nodKhrnDdJK9/kg2XD1r9uGqPo1cUbujc+IYdlYdEErWNu69gVcYgdxlmVmzTWnetw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <div class="newsletter">
       <i><h1 class="newsletter h2">Get updates about new abaya collections</h1>
            <p class="newsletter p "> Subscribe to our newsletter!</p>
        <input class="newsletter-email" type="text" placeholder=" Please Enter Your Email" required/>
         <button class="newsletter button newsletter button:hover ">Subscribe</button></i><a href="https://www.instagram.com/accounts/login/?next=%2Fmodestyelegance.com.pk%2Fprofilecard%2F&source=omni_redirect"><i  class=" icons fa-brands fa-instagram "></i></a><a href="https://www.facebook.com/people/Modesty-Elegance/61554901838608/?mibextid=wwXIfr&rdid=JU7fZyqLnk5wE2yk&share_url=https%3A%2F%2Fwww.facebook.com%2Fshare%2F19swz5WnuF%2F%3Fmibextid%3DwwXIfr"><i class="icons fa-brands fa-facebook"></i></a><a href="https://github.com/Maria-khan448"><i class="icons fa-brands fa-github"></i></a><a href="https://x.com/abayas_shop"><i class="icons fa-brands fa-x-twitter"></i></a><a href="https://api.whatsapp.com/send/?phone=923242252319&text&type=phone_number&app_absent=0"><i class="icons fa-brands fa-whatsapp"></i></a><a href="https://www.tiktok.com/@modestyelegance.com.pk"><i class="icons fa-brands fa-tiktok"></i></a>
    </div>
</template>

<style scoped >
/* newsLetter-component */
.newsletter{
  background-color:  rgba(0,0,0,0.9);
  padding: 60px;
  text-align: center;
  color: #F3F6F0;
  margin-top: 30px;
  border-radius: 5px;
}
.newsletter h2{
 font-size: 28px;
 margin-bottom: 10px;
}

.newsletter p{
 color: #ccc;
 font-size: 25px;
 font-weight: 600;
}

.newsletter-email{
  border-radius: 7px;
  padding: 15px 15px;
  width: 300px;
  margin-right: 10px;
   border: none;
}
.newsletter button{
 padding: 15px 15px;
 background-color: white;
 color: black;
 border: none;
 border-radius: 5px;
 cursor: pointer;
 width: 150px;
}

.newsletter button:hover{
 background-color: #a19c9c;
}

.icons{
  font-size: 30px;
  color: #ccc;
  gap: 6px;
  padding-left: 10px;
}
@media (max-width: 768px){
    .icons{
  font-size: 20px;
  color: #ccc;
  gap: 3px;
  padding-left: 10px;
}
.newsletter-email{
  width: 250px;
  margin-top: 15px;
  margin-right: 38px;
   border: none;
}
.newsletter button{

 width: 110px;
}
.newsletter h2{
 font-size: 10px;
 font-weight: 100;
 margin-bottom: 10px;
}
}
</style>