<template>
  <div class="container">
    <Navbar />
    <nuxt />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar'

export default {
  components: { Navbar }
}
</script>

<style scoped>
.container {
  width: 100vw;
  display: flex;
  flex-direction: column;
}
</style>
