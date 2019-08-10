<template>
  <div class="real-wrapper">
    <div class="real-container">
      <div class="header">
        <h1>Przykładowe realizacje</h1>
        <img class="hand-icon" src="../assets/images/Handshake.svg" />
      </div>
      <div class="cards-container">
        <Card v-for="card of cards" :key="card" class="card" />
      </div>
    </div>
    <img class="wave" src="../assets/images/Wave.svg" alt />
  </div>
</template>

<script>
import Card from '~/components/Card'

export default {
  components: {
    Card
  },
  data() {
    return {
      cards: [1, 2, 3, 4]
    }
  }
}
</script>

<style>
.real-container {
  margin: 30px auto;
  width: 80%;
}
.header {
  display: flex;
  align-items: center;
  margin-bottom: 40px;
}

.cards-container {
  display: flex;
}

.card {
  margin-right: 70px;
}

.hand-icon {
  width: 50px;
  margin-left: 10px;
  transform: translateY(35px);
}

.wave {
  position: absolute;
  bottom: -80px;
  left: 0;
  width: 100vw;
}
</style>
