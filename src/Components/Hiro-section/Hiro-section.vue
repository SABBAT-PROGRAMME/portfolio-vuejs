<!-- tamplete -->
<template>
  <!-- Desktop -->
  <section id="hiro">
    <div class="card desktop" id="hiro-section">
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
        <div
          v-for="item in listImages"
          :key="item.key"
          class="heroImageWrapper"
          @mouseover="showSecondImage"
          @mouseleave="showFirstImage"
        >
          <img :src="item.profile4" alt="sabbat" className="heroImage" />
          <!-- <img
          v-else
          :src="item.profile3"
          alt="sabbat"
          className="heroImageHover"
        /> -->
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="card">
      <div class="hero mobile">
        <div class="heroContent">
          <h2 class="greeting">{{ text[0].name }}</h2>
          <div
            v-for="item in listImages"
            :key="item.key"
            class="heroImageWrapper"
          >
            <img
              v-if="isFirstImageVisible"
              :src="item.profile4"
              alt="sabbat"
              className="heroImage"
            />
            <img
              v-else
              :src="item.profile3"
              alt="sabbat"
              className="heroImageHover"
            />
          </div>
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
      </div>
    </div>
  </section>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
import { listImages } from "../../assets/Css/Data/Data";
const text = [
  {
    name: "Hello I'm Sabbat Lumpatshia",
    title: "Full Stack",
    subTitle: "Developer",
    contact: "Contact me",
  },
];

const isFirstImageVisible = ref(true);
const showFirstImage = () => {
  isFirstImageVisible.value = true;
};
const showSecondImage = () => {
  isFirstImageVisible.value = false;
};
</script>

<!-- style -->
<style scoped>
/* Google Fonts */
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

html {
  scroll-behavior: smooth;
}

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
  position: relative;
  overflow: hidden;
  box-shadow: 0px 4px 25px rgba(14, 36, 49, 0.15);
}
.heroImageWrapper img {
  transition: 1s;
}
.heroImageWrapper img:hover {
  transform: scale(1.1);
}

.heroImage {
  /* position: absolute; */
}
img {
  border-radius: 13%;
}

.mobile {
  display: none;
}

/* responsive */
@media screen and (max-width: 768px) {
  .desktop {
    display: none;
  }
  .mobile {
    display: flex;
  }
  .hero {
    flex-direction: column-reverse;
    gap: 0;
  }
  .heroContent {
    align-items: center;
  }
  img {
    border-radius: 0%;
  }
  .heroImageWrapper {
    border-radius: 1%;
  }
  .title {
    color: #a6bbcc;
    font-size: 50px;
    line-height: 116px;
    font-weight: 900;
    font-family: "Poppins", system-ui;
    line-height: 1.2;
  }
  .heroImageWrapper {
    width: 300px;
  }
  .greeting {
    text-align: center;
    line-height: 1.2;
  }
  img {
    border-radius: 3%;
    margin: 15px 0px 15px 0px;
  }
}
</style>
