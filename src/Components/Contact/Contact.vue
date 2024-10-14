<!-- tamplete -->
<template>
  <section id="contact">
    <div class="contact" id="section-contact">
      <div class="title-contact">
        <div class="title"><h2>Contact</h2></div>
        <div class="content">
          <img
            src="https://cdn.builder.io/api/v1/image/assets/TEMP/8399dd158552add6a0df9eda0a80552af269a82ca42f72340631cc313b48a238?placeholderIfAbsent=true&apiKey=05e50562800e46f288f7d79b65b333f2"
            alt=""
            class="decorativeImage"
          />
          <div v-for="item in icones" :key="item.key" class="description">
            <ul
              v-for="(data, index) in data"
              class="timeline timeline-vertical"
            >
              <li>
                <div class="timeline-start">{{ data.emailtitle }}</div>
                <div class="timeline-middle">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    class="h-5 w-5"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
                      clip-rule="evenodd"
                    />
                  </svg>
                </div>
                <div class="timeline-end timeline-box">{{ data.email }}</div>
                <hr />
              </li>
              <li>
                <hr />
                <div class="timeline-start">{{ data.phonetitle }}</div>
                <div class="timeline-middle">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    class="h-5 w-5"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
                      clip-rule="evenodd"
                    />
                  </svg>
                </div>
                <div class="timeline-end timeline-box">{{ data.phone }}</div>
                <hr />
              </li>
              <li>
                <hr />
                <div class="timeline-start">{{ data.addresstitle }}</div>
                <div class="timeline-middle">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    class="h-5 w-5"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
                      clip-rule="evenodd"
                    />
                  </svg>
                </div>
                <div class="timeline-end timeline-box">
                  {{ data.address }}
                </div>
                <hr />
              </li>
              <li>
                <hr />
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- form -->
      <Form />
    </div>
  </section>

  <!-- section -->
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
import { icones } from "../../assets/Css/Data/Data";
import Form from "./Form.vue";

const data = [
  {
    emailtitle: "Email",
    email: "slmsabbat@gmail",
    phonetitle: "Phone",
    phone: "+243 828 829 232",
    addresstitle: "Address",
    address: "Limeté, Kinshasa, RDC",
  },
];
</script>

<!-- style -->
<style scoped>
html {
  scroll-behavior: smooth;
}
.contact {
  width: 100%;
  max-width: 1238px;
  margin: 101px auto 0;
  padding: 0 12px;
}
.title-contact {
  display: flex;
  gap: 70px;
  width: 100%;
  max-width: 1237px;
  margin: 0 auto;
  justify-content: center;
}
.title {
  color: #a6bbcc;
  font: 700 75px/2 Poppins, sans-serif;
}
.content {
  display: flex;
  flex-direction: column;
  margin: 20px;
}
.content img {
  font-weight: 900;
  padding-top: 60px;
  padding-bottom: 50px;
}
.container-icon {
  display: flex;
  align-items: center; /* Aligne l'image et le texte verticalement */
}
.description {
  color: #fff;
  font: 400 24px/44px Poppins, -apple-system, Roboto, Helvetica, sans-serif;
  max-width: 500px;
}

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

@media (max-width: 768px) {
  .title-contact {
    flex-direction: column;
    gap: 0;
  }
  .title {
    text-align: center;
    font-size: 40px;
  }
  .description {
    text-align: justify;
  }
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
  .contact {
    padding: 40px 20px;
  }

  .sectionTitle {
    font-size: 40px;
  }

  .description {
    font-size: 18px;
    line-height: 24px;
  }

  .submitButton::after {
    width: 180px;
  }
}

/* Style de la chronologie verticale */
.timeline {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
}

.timeline li {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.timeline-start {
  width: 100px;
  text-align: right;
  padding-right: 10px;
  font-weight: bold;
}

.timeline-middle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 30px;
  margin-right: 10px;
}

.timeline-end {
  background-color: #1f2937; /* Couleur du fond */
  padding: 10px 20px;
  border-radius: 20px;
  color: white;
  max-width: 200px;
  word-wrap: break-word;
}

hr {
  border: none;
  border-top: 1px solid #ccc;
  width: 100%;
  margin: 10px 0;
}

.timeline-box {
  background-color: #1f2937;
  color: white;
  padding: 10px 20px;
  border-radius: 10px;
}

h5 {
  font-size: 16px;
  margin: 0;
}

svg {
  width: 20px;
  height: 20px;
  color: #10b981; /* Change la couleur de l'icône */
}

.timeline li:last-child hr {
  display: none;
}
</style>
