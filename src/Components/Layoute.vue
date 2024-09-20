<!-- template -->

<template>
  <div id="layout">
    <Header />
    <HiroSection />
    <About />
    <Work />
    <Contact />
    <Footer />
  </div>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
import Header from "./Header/Header.vue";
import HiroSection from "./Hiro-section/Hiro-section.vue";
import About from "./About/About.vue";
import Work from "../Components/Work/Work.vue";
import Contact from "../Components/Contact/Contact.vue";
import Footer from "./Footer/Footer.vue";
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
#layout {
  margin: ;
}
</style>
