<!-- tamplete -->
<template>
  <div id="work" class="work">
    <div class="title-work">
      <h2 class="title">Work</h2>
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

    <div class="portfolioGrid">
      <div
        v-for="(item, index) in listImages"
        :key="index"
        class="portfolioItem"
      >
        <a href="#">
          <img
            :src="item.portfolio2"
            alt="Design Portfolio"
            class="portfolioImage"
        /></a>
        <h3 class="portfolioTitle">DESIGN PORTFOLIO</h3>
        <ul class="list-style-type: none; list-item">
          <li v-for="(item, index) in items" :key="index">
            {{ item.html }} {{ item.css }} {{ item.js }} {{ item.react }}
          </li>
        </ul>
      </div>
      <div
        v-for="(item, index) in listImages"
        :key="index"
        class="portfolioItem"
      >
        <a href="#"
          ><img
            :src="item.portfolio1"
            alt="Design Portfolio"
            class="portfolioImage"
        /></a>
        <h3 class="portfolioTitle">DESIGN PORTFOLIO</h3>
        <ul class="list-style-type: none; list-item">
          <li>HTML</li>
          <li>CSS</li>
          <li>JS</li>
          <li>React</li>
        </ul>
      </div>
    </div>
    <div></div>
  </div>
</template>

<!-- script -->
<script setup>
import { listImages } from "../Data/Data";
const items = [
  {
    html: "HTML",
    css: "CSS",
    js: "JS",
    react: "REACT",
  },
];
</script>

<!-- style -->
<style scoped>
.work {
  width: 100%;
  max-width: 1238px;
  margin: 101px auto 0;
  padding: 0 12px;
}

.title {
  color: #a6bbcc;
  font: 800 75px/2 Poppins, sans-serif;
}

.title-work {
  display: flex;
  gap: 80px;
  width: 100%;
  max-width: 1237px;
  margin: 0 auto;
  justify-content: center;
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

.decorativeImage {
  width: 100%;
  height: auto;
  margin-bottom: 17px;
}

.description {
  color: #fff;
  font: 400 24px/44px Poppins, -apple-system, Roboto, Helvetica, sans-serif;
  max-width: 900px;
}

.portfolioGrid {
  display: flex;
  gap: 20px;
  margin-top: 66px;
  row-gap: 2rem;
}

.portfolioItem {
  flex: 1;
  box-shadow: 0px 4px 25px rgba(14, 36, 49, 0.15);
  border-radius: 0.5rem;
  overflow: hidden;
}

.portfolioItem img {
  transition: 1s;
}
.portfolioItem img:hover {
  transform: scale(1.1);
}
.portfolioImage {
  width: 100%;
  aspect-ratio: 1.8;
  object-fit: contain;
}

.portfolioTitle {
  color: #fff;
  font: 700 24px/1 Space Grotesk, -apple-system, Roboto, Helvetica, sans-serif;
  margin-top: 31px;
  margin-left: 25px;
}

.list-item {
  display: flex;
  gap: 20px;
  margin-top: 15px;
  margin-left: 25px;
  font: 700 20px/1 Space Grotesk, -apple-system, Roboto, Helvetica, sans-serif;
}

@media (max-width: 768px) {
  .title-work {
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
  .portfolioGrid {
    flex-direction: column;
  }
}
</style>
