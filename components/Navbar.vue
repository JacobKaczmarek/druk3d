<template>
  <div class="navbar-container">
    <nav>
      <div class="logo-link-container">
        <nuxt-link to="/" class="logo">
          <span>Druk3D</span>
          <img src="~/assets/images/Logo.svg" alt="Logo" />
        </nuxt-link>
      </div>
      <ul class="nav-links">
        <li @click="closeMenu()">
          <nuxt-link to="oferta">Oferta</nuxt-link>
        </li>
        <li @click="closeMenu()">
          <nuxt-link to="realizacje">Realizacje</nuxt-link>
        </li>
        <li @click="closeMenu()">
          <nuxt-link to="contact">Kontakt</nuxt-link>
        </li>
      </ul>
      <div class="burger" @click="toggleNav()">
        <img src="../assets/images/Burger.svg" class="burger-icon" />
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  methods: {
    toggleNav() {
      document.querySelector('.nav-links').classList.toggle('open')
    },
    closeMenu() {
      document.querySelector('.nav-links').classList.remove('open')
    }
  }
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
  width: 100px;
}

.logo > img {
  margin: 5px;
  width: 25px;
}

.burger {
  display: none;
  cursor: pointer;
}

ul {
  display: flex;
  justify-content: space-evenly;
  width: 40%;
  list-style: none;
}

li {
  margin: 35px 20px;
  font-size: 20px;
}

a {
  text-decoration: none;
  color: inherit;
}

.nuxt-link-active {
  color: black;
}

@media screen and (max-width: 765px) {
  nav {
    height: 100%;
    flex-direction: column;
    color: white;
  }

  .nav-links {
    position: absolute;
    height: 100%;
    width: 100vw;

    z-index: 2;
    background: #51c4f5;
    margin: auto;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    clip-path: circle(0 at 110% -10%);
    -webkit-clip-path: circle(0 at 110% -10%);
    transition: all 0.3s ease-out;
  }

  .open {
    clip-path: circle(1000px at 95% 5%);
    -webkit-clip-path: circle(1000px at 95% 5%);
    transition: all 0.7s ease-out;
  }

  .burger {
    position: absolute;
    top: 5%;
    right: 5%;
    display: block;
    z-index: 3;
  }
}
</style>
