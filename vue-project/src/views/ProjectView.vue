<template> 
<div class="contact-form">
  <h1 style="background-color: yellowgreen;">Contact Form</h1>
  <form @submit.prevent="submitForm">
    <label for="name">Name:</label>
    <input id="name" v-model="formData.name" required placeholder="Enter your name">
    
    <label for="email">Email:</label>
    <input id="email" v-model="formData.email" type="email" required placeholder="Enter your e-mail">

    <label for="message">Message:</label>
    <textarea id="message" v-model="formData.message" rows="4" required placeholder="Drop a message for me"></textarea>

    <button type="submit" class="submit-button">Submit</button>
  </form>
</div>

</template>

<script>
export default {
data() {
  return {
    formData: {
      name: '',
      email: '',
      message: ''
    }
  };
},
methods: {
  submitForm() {
    console.log('Form Data:', this.formData);
    alert('Form submitted successfully!');
  }
}
}
</script>


<style>
body, h1, h2, p, label, input, textarea, button {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
  }
  
  #app {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color:greenyellow;
  }
  
  .contact-form {
    background-color:greenyellow;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 90%;
  }
  
  label {
    font-weight: bold;
    display: block;
    margin-bottom: 5px;
    font-family:'Pacifico', cursive;
  }
  
  input[type="text"],
  input[type="email"],
  textarea {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    transition: border-color 0.3s;
  }
  
  input[type="text"]:focus,
  input[type="email"]:focus,
  textarea:focus {
    border-color: #007bff;
  }
  
  textarea {
    resize: vertical;
  }
  
  .submit-button {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
  }
  
  @media (max-width: 768px) {
    .contact-form {
      width: 100%;
      padding: 20px;
    }
  }
</style>







