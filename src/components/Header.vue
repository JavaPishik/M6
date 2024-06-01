<template>
  <header>
    <router-link to="/">Main</router-link>
    <router-link to="/fantasy">Fantasy</router-link>
    <router-link to="/royale">Royale</router-link>
    <router-link to="/rpg">Rpg</router-link>
    <router-link to="/shooter">Shooter</router-link>
    <router-link to="/strategy">Strategy</router-link>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-evenly;
  padding: 20px;
  font-size: 30px;
  color: #d1bdff;
  background: #292f32;
}
.router-link-active {
  color: #aaa;
  font-size: 35px;
}
</style>
