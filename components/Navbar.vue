<template>
  <div class="container">
    <nav>
      <div class="logo">
        <span>Druk3D</span>
        <img src="~/assets/images/Logo.svg" alt="Logo" />
      </div>
      <ul>
        <li>
          <a href>Oferta</a>
        </li>
        <li>
          <a href>Realizacje</a>
        </li>
        <li>
          <a href>Kontakt</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>
.container {
  width: 100vw;
  text-align: center;
}

nav {
  color: #535353;
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.logo {
  display: flex;
  align-items: center;
  font-weight: 600;
  margin: 35px;
  font-size: 20px;
}

.logo > img {
  margin: 5px;
  width: 25px;
}

ul {
  display: flex;
  justify-content: space-evenly;
  width: 40%;
  list-style: none;
}

li {
  margin: 35px;
  font-size: 20px;
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
