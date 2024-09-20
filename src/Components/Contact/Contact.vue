<!-- tamplete -->
<template>
  <div class="contact" id="section-contact">
    <div class="title-contact">
      <div class="title"><h2>Contact</h2></div>
      <div class="content">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/8399dd158552add6a0df9eda0a80552af269a82ca42f72340631cc313b48a238?placeholderIfAbsent=true&apiKey=05e50562800e46f288f7d79b65b333f2"
          alt=""
          class="decorativeImage"
        />
        <p class="description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Amet
          vulputate tristique quam felis. Id phasellus dui orci vulputate
          consequat nulla proin. Id sit scelerisque neque, proin bibendum diam.
        </p>
      </div>
    </div>
    <!-- form -->
    <form className="contactForm">
      <div className="formGroup">
        <label htmlFor="name" className="visuallyHidden">Name</label>
        <input
          type="text"
          id="name"
          name="name"
          placeholder="NAME"
          required
          className="formInput"
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
        ></textarea>
      </div>
      <div className="btn-submit">
        <button type="submit" className="submitButton">SEND MESSAGE</button>
      </div>
    </form>
  </div>

  <!-- section -->
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
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
.description {
  color: #fff;
  font: 400 24px/44px Poppins, -apple-system, Roboto, Helvetica, sans-serif;
  max-width: 900px;
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
</style>
