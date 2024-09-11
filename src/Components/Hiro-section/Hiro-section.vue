<script setup>
import { ref } from "vue";
const text = [
  {
    name: "Hello I'm Sabbat Lumpatshia",
    title: "Full Stack",
    subTitle: "Developer",
    contact: "Contact me",
  },
];
</script>

<template>
  <div class="card">
    <div class="hero">
      <div class="heroContent">
        <h2 class="greeting">{{ text[0].name }}</h2>
        <h1 class="title">
          {{ text[0].title }}<br />
          {{ text[0].subTitle }}
        </h1>
        <a href="#contact" class="contactButton">{{ text[0].contact }}</a>
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/1b2696c4afe8a807e21e0d063c6b116dfe5122a64dc8d1b58863aeb7ec5e3c08?placeholderIfAbsent=true&apiKey=05e50562800e46f288f7d79b65b333f2"
          alt=""
          class="decorativeImage"
        />
      </div>
      <div class="heroImageWrapper">
        <img src="../../../public//images/sabbat.png" className="heroImage" />
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Google Fonts */
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

.card {
  display: flex;
  justify-content: center;
}
.hero {
  display: flex;
  gap: 120px;
  padding: 2rem 0;
  justify-content: center;
}

.heroContent {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  font-family: Poppins, sans-serif;
  color: #fff;
}

.greeting {
  font-size: 28px;
  font-weight: 500;
}

.title {
  color: #a6bbcc;
  font-size: 100px;
  line-height: 116px;
  font-weight: 900;
  font-family: "Poppins", system-ui;
}

.contactButton {
  font-size: 28px;
  font-weight: 500;
}

.decorativeImage {
  width: 150px;
  margin-top: 15px;
}
.heroImageWrapper {
  width: 500px;
  border-radius: 13%;
}
img {
  border-radius: 13%;
}
</style>
