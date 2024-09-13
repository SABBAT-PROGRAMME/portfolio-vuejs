<!-- template -->

<template>
  <div id="layout">
    <Header />
    <HiroSection />
    <About />
    <Work />
  </div>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
import Header from "./Header/Header.vue";
import HiroSection from "./Hiro-section/Hiro-section.vue";
import About from "./About/About.vue";
import Work from "../Components/Work/Work.vue";
</script>

<style scoped>
#layout {
  margin: ;
}
</style>
