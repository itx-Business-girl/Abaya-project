<template>
  
<div class="contact-section">

<h2 class="contact-heading">Contact Us</h2>
<p class="contact-text">
Feel free to send us a message. We will reply as soon as possible.
</p>

<form class="contact-form" @submit.prevent="sendMessage">

<input type="text" placeholder="Enter Your Name" v-model="name"/>
<input type="email" placeholder="Enter Your Email" v-model="email"/>
<textarea placeholder="Your Message" v-model="message"></textarea>

<button type="submit">Send Message</button>

</form>

</div>
</template>

<script setup>

import { ref } from "vue"

const name = ref("")
const email = ref("")
const message = ref("");

const sendMessage = async () => {

const formData = {
name: name.value,
email: email.value,
message: message.value
}

console.log("FormData:", formData)

try{

const response = await fetch("https://fakestoreapi.com/products",{
method:"POST",
headers:{
"Content-Type":"application/json"
},
body: JSON.stringify(formData)
})

const data = await response.json()

console.log("Server Response:", data)

alert("Congratulations Your Message successfully sent!")

}catch(error){

console.error(error)
alert("Something went wrong!")

}

}
</script>

<style scoped>

/* Contact Section */
.contact-section{
max-width: 600px;
margin: auto;
padding: 50px 20px;
text-align: center;
}

/* Heading */
.contact-heading{
font-size: 32px;
margin-bottom: 10px;
}

/* Text */
.contact-text{
color: gray;
margin-bottom: 30px;
}

/* Form Styling */
.contact-form{
display: flex;
flex-direction: column;
gap: 15px;
}

/* Inputs */
.contact-form input,
.contact-form textarea{
padding: 12px;
border-radius: 6px;
border: 1px solid #ddd;
font-size: 15px;
}

/* Textarea height */
.contact-form textarea{
height: 120px;
resize: none;
}

/* Button */
.contact-form button{
padding: 12px;
background: black;
color: white;
border: none;
border-radius: 6px;
font-size: 16px;
cursor: pointer;
}

.contact-form button:hover{
background: #222;
}

</style>