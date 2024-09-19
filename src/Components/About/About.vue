<!-- tamplete -->
<template>
  <!-- About -->
  <div class="about">
    <h2 class="title">About</h2>
    <div class="content">
      <img
        src="https://cdn.builder.io/api/v1/image/assets/TEMP/3892a4af946c81724f28289282891482f75f09fae7c15125817bbad1a0abd657?placeholderIfAbsent=true&apiKey=05e50562800e46f288f7d79b65b333f2"
        alt=""
        className="decorativeImage"
      />
      <p className="description">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Amet vulputate
        tristique quam felis. Id phasellus dui orci vulputate consequat nulla
        proin. Id sit scelerisque neque, proin bibendum diam.
      </p>
    </div>
  </div>

  <!-- skills -->
  <div class="skills">
    <div v-for="(skill, index) in skillsData" :key="index" class="skillItem">
      <h3 class="skillTitle">{{ skill.title }}</h3>
      <p class="skillExperience">{{ skill.experience }}</p>
      <div class="skillBar"></div>
    </div>
  </div>
</template>

<!-- script -->
<script setup>
const skillsData = [
  { title: "Front-End", experience: "60+ Hours Experience" },
  { title: "Python", experience: "4 Years Experience" },
  { title: "Machine Learning", experience: "120+ Hours Experience" },
];
</script>

<!-- style -->
<style scoped>
html {
  scroll-behavior: smooth;
}
.about {
  width: 100%;
  max-width: 1237px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  gap: 15px;
}

.title {
  color: #a6bbcc;
  font: 800 75px/2 Poppins, sans-serif;
}

.content {
  display: flex;
  flex-direction: column;
  width: 47%;
  margin: 20px;
}

img {
  font-weight: 900;
  padding-top: 50px;
  padding-bottom: 50px;
}

.decorativeImage {
  width: 100%;
  height: auto;
}

.description {
  color: #fff;
  font: 400 24px/44px Poppins, -apple-system, Roboto, Helvetica, sans-serif;
  margin-top: 15px;
}

@media (max-width: 991px) {
  .title {
    font-size: 40px;
  }
}

/* skills */
.skills {
  display: flex;
  width: 100%;
  max-width: 1091px;
  margin: 88px auto 0;
  gap: 20px;
  font-family: Space Grotesk, -apple-system, Roboto, Helvetica, sans-serif;
  text-align: center;
  flex-wrap: wrap;
  justify-content: space-between;
}

.skillItem {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.skillTitle {
  color: #fff;
  font-size: 48px;
  font-weight: 700;
  line-height: 1;
  letter-spacing: -1.5px;
}

.skillExperience {
  color: #d9d9d9;
  font-size: 18px;
  font-weight: 500;
  line-height: 2;
  margin-top: 14px;
}

.skillBar {
  background-color: #a6bbcc;
  width: 190px;
  height: 2px;
  margin-top: 14px;
}

@media screen and (max-width: 768px) {
  .about {
    flex-direction: column;
    align-items: center;
    width: 100%;
  }
  img {
    padding-top: 5px;
    padding-bottom: 5px;
  }
  .description {
    text-align: justify;
    font-size: 3em;
    width: 100%;
  }
  .skills {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.skills h3 {
  font-size: 36px;
}
.content {
  display: flex;
  flex-direction: column;
  width: 90%;
  margin: 20px;
  font-size: 0.5em;
}
</style>
