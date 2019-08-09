<template>
  <div class="container">
    <img class="hero" src="../assets/images/Hero.svg" alt />
    <h1>Druk 3d na który cie stać</h1>
    <h3>Realizuj pomysły nie płacąc fortuny.</h3>
    <button class="offer-btn">Sprawdz oferte</button>
  </div>
</template>

<script>
export default {
  components: {}
}
</script>

<style>
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

h1 {
  font-weight: normal;
  margin-top: 40px;
}

h3 {
  color: #363636;
  font-weight: normal;
  margin-top: 15px;
}

.offer-btn {
  font-size: 28px;
  color: white;
  background: #51c4f5;
  margin: 50px;
  padding: 15px 20px;
}
</style>
