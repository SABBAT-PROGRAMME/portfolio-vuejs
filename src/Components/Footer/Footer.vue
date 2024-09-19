<!-- tamplete -->
<template>
  <footer className="footer">
    <!-- <h2 className="logo">
      Sabbat<span className="logoLight">Lumpatshia</span>
    </h2> -->
    <div class="flex title flex-shrink-0 items-center title-desktop">
      <span
        ><strong> Sabbat </strong> <span class="myName">Lumpatshia</span></span
      >
    </div>
    <div>
      <p class="footer__copy">&#169; Sabbat Lumpatshia. Tous droits réservés</p>
    </div>
    <div v-for="(item, index) in icones" :key="index" className="socialLinks">
      <a href="#" aria-label="GitHub profile">
        <img :src="item.linkedin" alt="" className="socialIcon" />
      </a>
      <a href="#" aria-label="GitHub profile">
        <img :src="item.facebook" alt="" className="socialIcon" />
      </a>
      <a href="#" aria-label="LinkedIn profile">
        <img :src="item.instagram" alt="" className="socialIcon" />
      </a>
      <a href="#" aria-label="Twitter profile">
        <img :src="item.github" alt="" className="socialIcon" />
      </a>
    </div>
  </footer>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
import { icones } from "../../assets/Css/Data/Data";
</script>

<!-- style -->
<style scoped>
html {
  scroll-behavior: smooth;
}
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 65px;
  margin-top: 45px;
  color: #fff;
}
.title {
  font-size: 1.9em;
}

.myName {
  color: #a6bbcc;
}

.logo {
  font: 700 32px Inter, sans-serif;
}

.logoLight {
  font-weight: 400;
}

.socialLinks {
  display: flex;
  gap: 17px;
}

.socialIcon {
  width: 40px;
  height: 40px;
}

@media (max-width: 991px) {
  .footer {
    flex-direction: column;
    gap: 20px;
    padding: 30px 20px;
  }
}
</style>
