<template>
  <nav class="nav">
    <router-link to="/">
      <p class="nav__logo">Logo</p>
    </router-link>
    <ul class="nav__menu">
      <li class="nav__item">
        <router-link data-text="home" to="/" class="nav__link">
          home
        </router-link>
      </li>
      <li class="nav__item">
        <router-link data-text="explore" to="/explore" class="nav__link">
          explore
        </router-link>
      </li>
      <li class="nav__item">
        <router-link data-text="favourites" to="/" class="nav__link">
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
  height: 10vh;
}

.nav__logo {
  flex: 0 0 20%;
}

.nav__menu {
  flex: 0 0 75%;
  display: flex;
  justify-content: space-between;
}

.nav__item {
  padding: 0 0.75rem;
}

.nav__link {
  position: relative;
  font-size: 1.6rem;
  color: #e5e5e5;
  transition: color 0.3s cubic-bezier(0.19, 1, 0.22, 1);
}


.nav__link:hover {
  color: #277c99;
}

@media screen and (max-width: 768px) {
  .nav {
    justify-content: center;
  }
  .nav__logo {
    display: none;
  }
  .nav__menu {
    flex: 0 0 90%;
  }
}

@media screen and (max-width: 360px) {
  .nav__link {
    font-size: 1.4rem;
  }
}
</style>
