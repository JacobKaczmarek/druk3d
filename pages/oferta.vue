<template>
  <div class="offer-wrapper">
    <div class="offer-container">
      <div class="left-container">
        <h1>Co robimy?</h1>
        <ul>
          <li>Lorem ipsum dolor sit amet consectetur.</li>
          <li>Lorem ipsum dolor sit amet consectetur.</li>
          <li>Lorem ipsum dolor sit amet consectetur.</li>
          <li>Lorem ipsum dolor sit amet consectetur.</li>
          <li>Lorem ipsum dolor sit amet consectetur.</li>
        </ul>
      </div>
      <img class="dino" src="../assets/images/dinosaur.png" />
    </div>
    <img class="wave" src="../assets/images/Wave.svg" alt />
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.offer-wrapper {
  width: 100vw;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.offer-container {
  display: flex;
  justify-content: space-between;
  margin-top: 80px;
  width: 60%;
}

.dino {
  width: 250px;
}

ul {
  color: #363636;
  margin-top: 25px;
  line-height: 1.8;
  letter-spacing: 0.1em;
}

.wave {
  position: absolute;
  bottom: -60px;
  left: 0;
  width: 100vw;
}
</style>
