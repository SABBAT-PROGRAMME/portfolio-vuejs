<!-- Tamplate -->
<template>
  <form className="contactForm" @submit.prevent="sendEmail">
    <div className="formGroup">
      <label htmlFor="name" className="visuallyHidden">Name</label>
      <input
        type="text"
        id="name"
        name="name"
        placeholder="NAME"
        required
        className="formInput"
        v-model="form.name"
      />
    </div>
    <div className="formGroup">
      <label htmlFor="email" className="visuallyHidden">Email</label>
      <input
        type="email"
        id="email"
        name="email"
        placeholder="EMAIL"
        required
        className="formInput"
        v-model="form.email"
      />
    </div>
    <div className="formGroup">
      <label htmlFor="message" className="visuallyHidden">Message</label>
      <textarea
        id="message"
        name="message"
        placeholder="MESSAGE"
        required
        className="formTextarea"
        v-model="form.message"
      ></textarea>
    </div>
    <div className="btn-submit">
      <button type="submit" className="submitButton">SEND MESSAGE</button>
      <p v-if="successMessage" class="success">{{ successMessage }}</p>
      <p v-if="errorMessage" class="error">{{ errorMessage }}</p>
    </div>
  </form>
</template>

<!-- script -->

<script setup>
import { ref } from "vue";
import emailjs from "emailjs-com";

// Créer l'état du formulaire avec les valeurs initiales
const form = ref({
  name: "",
  email: "",
  message: "",
});

// Variables pour afficher les messages de succès ou d'erreur
const successMessage = ref("");
const errorMessage = ref("");

// Fonction pour envoyer l'email avec EmailJS
const sendEmail = () => {
  emailjs
    .send(
      "sabbat_service", // Remplacez par votre Service ID EmailJS * service_r4ewqzc
      "template_kt0r0j1", // Remplacez par votre Template ID EmailJS
      {
        from_name: form.value.name,
        from_email: form.value.email,
        message: form.value.message,
      },
      "YOUR_USER_ID" // Remplacez par votre User ID EmailJS
    )
    .then(
      (response) => {
        console.log("SUCCESS!", response.status, response.text);
        successMessage.value = "Votre message a été envoyé avec succès !";
        form.value = { name: "", email: "", message: "" };
      },
      (err) => {
        console.error("FAILED...", err);
        errorMessage.value =
          "Une erreur s'est produite lors de l'envoi de l'email.";
      }
    );
};
</script>

<!-- style -->
<style>
.btn-submit {
  overflow: hidden;
}
.btn-submit button {
  transition: 1s;
}
.btn-submit button:hover {
  border-color: #fff;
  color: #a6bbcc;
  background: #fff;
}

.contactForm {
  max-width: 748px;
  margin: 0 auto;
}

.formGroup {
  margin-bottom: 40px;
}

.visuallyHidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
Textarea,
input {
  outline: none;
}

.formInput,
.formTextarea {
  width: 100%;
  background: transparent;
  border: none;
  border-bottom: 2px solid #fff;
  color: #fff;
  font: 500 16px/2 Space Grotesk, sans-serif;
  padding: 10px 0;
}

.formInput::placeholder,
.formTextarea::placeholder {
  color: rgba(255, 255, 255, 0.5);
}

.formTextarea {
  min-height: 100px;
  resize: vertical;
}

.btn-submit {
  display: flex;
  justify-content: center;
}

button[type="submit"] {
  padding: 15px;
  border-radius: 2%;
}
.submitButton {
  background: transparent;
  border: 1px solid #a6bbcc;
  padding: 10px;
  color: #fff;
  font: 700 16px/2 Space Grotesk, sans-serif;
  letter-spacing: 2.29px;
  cursor: pointer;
  padding: 10px 0;
  position: relative;
}

@media (max-width: 991px) {
  .submitButton::after {
    width: 180px;
  }
}
</style>

<style scoped>
.contact-form {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 8px;
}

.contact-form h2 {
  text-align: center;
  color: #333;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

/* .btn-submit {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
} */
/* 
.btn-submit:hover {
  background-color: #0056b3;
} */

.success {
  color: green;
  text-align: center;
  margin-top: 10px;
}

.error {
  color: red;
  text-align: center;
  margin-top: 10px;
}
</style>
