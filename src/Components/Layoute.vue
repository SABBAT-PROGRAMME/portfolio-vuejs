<!-- template -->

<template>
  <div id="layout">
    <Header />
    <HiroSection id="hiro" />
    <About id="about" />
    <Work id="work" />
    <Contact id="contact" />
    <router-view />
    <Footer />
  </div>
</template>

<!-- script -->

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

import Header from "./Header/Header.vue";
import HiroSection from "./Hiro-section/Hiro-section.vue";
import About from "./About/About.vue";
import Work from "../Components/Work/Work.vue";
import Contact from "../Components/Contact/Contact.vue";
import Footer from "./Footer/Footer.vue";

const sections = ref([]);
function scrollActive() {
  const scrollY = window.pageYOffset;
  sections.value.forEach((current) => {
    const sectionHeight = current.offsetHeight;
    const sectionTop = current.offsetTop - 50;
    const sectionId = current.getAttribute("id");

    const link = document.querySelector(`.nav__menu a[href*=${sectionId}]`);
    if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {
      link?.classList.add("active");
    } else {
      link?.classList.remove("active");
    }
  });
}

onMounted(() => {
  // Sélectionne toutes les sections avec un id
  sections.value = document.querySelectorAll("section[id]");
  // Ajoute l'événement de scroll
  window.addEventListener("scroll", scrollActive);
});

// Nettoie l'événement au démontage
onBeforeUnmount(() => {
  window.removeEventListener("scroll", scrollActive);
});
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
</style>
