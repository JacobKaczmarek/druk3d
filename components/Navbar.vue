<template>
  <div class="navbar-container">
    <nav>
      <nuxt-link to="/" class="logo">
        <span>Druk3D</span>
        <img src="~/assets/images/Logo.svg" alt="Logo" />
      </nuxt-link>
      <ul>
        <li>
          <nuxt-link to="oferta">Oferta</nuxt-link>
        </li>
        <li>
          <a href>Realizacje</a>
        </li>
        <li>
          <nuxt-link to="contact">Kontakt</nuxt-link>
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
.navbar-container {
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

.nuxt-link-active {
  color: black;
}
</style>
