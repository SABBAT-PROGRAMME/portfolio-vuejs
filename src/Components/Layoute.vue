<template>
  <div class="bg-blue-500 text-white p-4 rounded-md shadow-md">
    <h1 class="text-2xl font-bold">{{ name }}</h1>
  </div>
  <button class="btn btn-primary">One</button>
  <button class="btn btn-secondary">Two</button>
  <button class="btn btn-accent btn-outline">Three</button>
</template>

<script setup>
const name = "Portfolio-Sabbat";
</script>

<style scoped>
body {
  background-color: white;
}
</style>
