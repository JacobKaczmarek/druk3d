<template>
  <div class="wave-container">
    <img class="wave" src="../assets/images/Wave.svg" alt />
  </div>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    offset: {
      type: String,
      default: '-80px'
    }
  },
  computed: {
    style() {
      return `bottom: ${this.offset}`
    }
  }
}
</script>

<style scoped>
.wave-container {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
}

.wave {
  position: absolute;
  left: 0;
  bottom: -50px;
  width: 100vw;
  z-index: -1;
}

@media screen and (max-width: 765px) {
  .wave {
    bottom: 0px;
  }
}
</style>
