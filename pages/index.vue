<template>
  <div class="container">
    <img class="hero" src="../assets/images/Hero.svg" alt />
    <h1>Druk 3D na który cie stać</h1>
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
  font-size: 35px;
  margin-top: 60px;
}

h3 {
  color: #363636;
  font-weight: normal;
  font-size: 18px;
  margin-top: 10px;
}

.offer-btn {
  font-size: 23px;
  color: white;
  background: #51c4f5;
  margin: 80px;
  padding: 10px 20px;
  border: none;
}
</style>
