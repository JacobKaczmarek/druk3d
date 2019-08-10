<template>
  <div class="container">
    <img class="hero" src="../assets/images/Hero.svg" alt />
    <h1>Druk 3D na który cie stać</h1>
    <h3>Realizuj pomysły nie płacąc fortuny.</h3>
    <nuxt-link to="oferta" class="offer-btn">Sprawdz oferte</nuxt-link>
  </div>
</template>

<script>
export default {
  components: {}
}
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  transform: translateX(20px);
}

.hero {
  margin-top: 50px;
  width: 300px;
  transform: translateX(55px);
}

.offer-btn {
  font-size: 23px;
  color: white;
  background: #51c4f5;
  margin: 80px;
  padding: 10px 20px;
  border: none;
  text-decoration: none;
}
</style>
