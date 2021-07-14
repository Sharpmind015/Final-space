<template>
  <nav class="nav">
    <router-link to="/">
      <p class="nav__logo">Logo</p>
    </router-link>
    <ul class="nav__menu">
      <li class="nav__item">
        <router-link class="nav__link">
          home
        </router-link>
      </li>
      <li class="nav__item">
        <router-link class="nav__link">
          explore
        </router-link>
      </li>
      <li class="nav__item">
        <router-link class="nav__link">
          favourites
        </router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.nav {
  position: relative;
  padding: 2rem 3rem;
  display: flex;
  justify-content: space-between;
}

.nav__logo {
  flex: 0 0 20%;
}

.nav__menu {
  flex: 0 0 75%;
  display: flex;
  justify-content: space-between;
}

.nav__link {
  font-size: 1.6rem;
  padding: 0 0.75rem;
}
</style>
