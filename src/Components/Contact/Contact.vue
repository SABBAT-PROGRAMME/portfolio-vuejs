<!-- tamplete -->
<template>
  <div class="contact">
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
  </div>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
</script>

<!-- style -->
<style scoped>
.contact {
  width: 100%;
  max-width: 1238px;
  margin: 101px auto 0;
  padding: 0 12px;
}
.title-contact {
  display: flex;
  /* gap: 80px; */
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
</style>
