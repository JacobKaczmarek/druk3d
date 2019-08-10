<template>
  <div class="card-container">
    <img :src="path" alt />
    <h3>{{ name }}</h3>
    <p>{{ price }}</p>
  </div>
</template>

<script>
export default {
  name: 'Card',
  data() {
    return {
      path: require('../assets/images/Falcon.png'),
      name: 'Name',
      price: '15.99'
    }
  }
}
</script>

<style scoped>
.card-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 200px;
  width: 200px;
}

img {
  width: 200px;
  border-radius: 3px;
}

p {
  font-size: 12px;
  color: #707070;
}
</style>
