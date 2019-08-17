<template>
  <div class="real-wrapper">
    <div class="header">
      <h1>Przykładowe realizacje</h1>
      <img class="hand-icon" src="../assets/images/Handshake.svg" />
    </div>
    <div class="real-container">
      <div class="cards-grid">
        <Card v-for="card of cards" :key="card" class="card" />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Card from '~/components/Card'
import Footer from '~/components/Footer'

export default {
  components: {
    Card,
    Footer
  },
  data() {
    return {
      cards: [1, 2, 3, 4, 5, 6, 7, 8]
    }
  }
}
</script>

<style scoped>
.real-container {
  margin: 30px auto;
  width: 80%;
  height: 55vh;
}

h1 {
  margin: 0;
}

.header {
  display: flex;
  align-items: center;
  width: 80%;
  margin: auto;
  margin-top: 40px;
}

.cards-grid {
  display: grid;
  grid-template-columns: auto auto auto auto;
  border-left: 2px solid #51c4f5;
  height: 300px;
  overflow-y: scroll;
}

.card {
  margin: 0 70px 60px 0;
}

.hand-icon {
  width: 50px;
  margin-left: 5px;
}

.wave {
  position: absolute;
  bottom: -80px;
  left: 0;
  width: 100vw;
}

.card {
  margin: 50px auto;
  justify-self: center;
}

@media screen and (max-width: 765px) {
  .header {
    margin: auto;
  }

  .cards-grid {
    grid-template-columns: auto;
    height: 300px;
  }
}
</style>
