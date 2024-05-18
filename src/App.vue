<script setup>
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import { RouterView } from "vue-router";
</script>

<template>
  <div class="app">
    <Header />
    <RouterView />
    <Card />
  </div>
</template>

<style scoped>
.app {
  background: #343b3f;
  min-height: 100vh;
}
</style>
