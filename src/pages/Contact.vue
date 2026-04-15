<template>
  
<div class="contact-section">

<h2 class="contact-heading">Contact Us</h2>
<p class="contact-text">
Feel free to send us a message. We will reply as soon as possible.
</p>

<form class="contact-form" @submit.prevent="handleSubmit">

<input type="text" placeholder="Enter Your Name" v-model="name"/>
<input type="email" placeholder="Enter Your Email" v-model="email"/>
<textarea placeholder="Your Message" v-model="message"></textarea>

<button type="submit">Send Message</button>
</form>
<!--  Toast -->
      <div v-if="showToast" class="toast">
        {{ toastMessage }}
      </div>
 


</div>
</template>

<script setup>
import { ref } from 'vue'

// form data
const name = ref('')
const email = ref('')
const message = ref('')

// toast state
const showToast = ref(false)
const toastMessage = ref('')

// email validation
const isValidEmail = (email) => {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)
}

// reusable toast function
const showMessage = (msg) => {
  toastMessage.value = msg
  showToast.value = true

  setTimeout(() => {
    showToast.value = false
  }, 3000)
}

// submit handler
const handleSubmit = () => {
  // debug (optional)
  console.log("Form submitted")

  // empty fields check
  if (!name.value || !email.value || !message.value) {
    showMessage("Please fill all fields")
    return
  }

  // email validation
  if (!isValidEmail(email.value)) {
    showMessage("Invalid Email Address")
    return
  }

  // success
  showMessage("Your message successfully sent")

  // reset form
  name.value = ''
  email.value = ''
  message.value = ''
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
/* toast */
 .toast{
   position: fixed;
  bottom: 20px;
  right: 20px;
  background: rgb(197, 183, 183);
  color: rgb(36, 35, 35);
  padding: 12px 18px;
  border-radius: 8px;
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
@media (max-width: 768px){
  .contact-heading{
font-size: 25px;
display: flex;
justify-content: flex-start;
align-items: flex-start;
margin-left: 15px;
margin-bottom: 10px;
  }
  .contact-text{
    font-size: 15px;
    margin-bottom: 20px;
  }
}

</style>