<script setup>
import { DetailGame } from "@/api";
import { useRoute } from "vue-router";
import { onBeforeMount, ref } from "vue";

let detail = ref();
let route = useRoute();

onBeforeMount(async () => {
  detail.value = await DetailGame(route.params.id);
});
</script>

<template>
  <section>
    <nav>
      <img
        v-for="(scren, index) in detail.screenshots"
        :key="index"
        :src="scren.image"
      />
    </nav>
    <h1>{{ detail.title }}</h1>
    <p>{{ detail.description }}</p>
  </section>
</template>

<style scoped>
section {
  padding: 10px;
}
img {
  border-radius: 16px;
  width: 47.5%;
  aspect-ratio: 16/9;
  transition: all 0.5s;
}
img:hover {
  transform: scale(1.05);
}
nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  grid-gap: 50px;
}
h1 {
  color: #aaa;
  font-size: 50px;
  text-align: center;
  margin-top: 20px;
}
p {
  color: #aaa;
  font-size: 24px;
  text-align: center;
  margin-top: 20px;
  margin-bottom: 50px;
  line-height: 1.2;
}
</style>
