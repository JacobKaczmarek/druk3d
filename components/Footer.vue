<template>
  <img :style="style" class="wave" src="../assets/images/Wave.svg" alt />
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
.wave {
  position: fixed;
  left: 0;
  width: 100vw;
}
</style>
