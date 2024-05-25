<script setup>
defineProps({
  game: Object,
});
</script>

<template>
  <div>
    <img :src="game.thumbnail" alt="" />
    <h1>{{ game.title }}</h1>
    <p>{{ game.short_description }}</p>
    <nav>
      <i class="far fa-calendar-minus"></i>
      <h4>{{ game.release_date }}</h4>
    </nav>
    <nav>
      <i class="fas fa-desktop"></i>
      <h4>{{ game.platform }}</h4>
    </nav>
    <button>Подробнее</button>
  </div>
</template>

<style scoped>
div {
  width: 100%;
  padding: 10px;
  display: flex;
  flex-direction: column;
  background: #1c242e;
  color: #aaa;
  border-radius: 10px;
  transition: all 0.5s;
}
div:hover {
  background: #482e44;
  transform: scale(1.05);
}
img {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  border-radius: 10px;
}
h1 {
  margin-top: 20px;
  font-size: 30px;
}
p {
  margin-top: 20px;
  font-size: 20px;
  line-height: 1.2;
}
nav {
  display: flex;
  margin-top: 20px;
  font-size: 20px;
}
i {
  margin-right: 10px;
}
button {
  background: #a889b1;
  font-size: 20px;
  padding: 10px 20px;
  margin-top: 20px;
  margin-left: auto;
  border-radius: 10px;
  transition: all 0.1s;
}
button:hover {
  background: #b799c0;
  transform: scale(0.95);
}
</style>
