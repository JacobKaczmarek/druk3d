<template>
  <div class="container">
    <nav>
      <div class="logo">Logo</div>
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
  margin: 35px;
}

ul {
  display: flex;
  justify-content: space-evenly;
  width: 40%;
  list-style: none;
}

li {
  margin: 35px;
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
