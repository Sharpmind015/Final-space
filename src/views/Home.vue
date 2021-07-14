<template>
  <main class="home">
    <section class="hero">
      <div class="hero__content">
        <h1 class="hero__heading">
          <div class="line-1">Final</div>
          <div class="line-2">Space</div>
        </h1>
        <p class="hero__tagline">Chookity pok pok pok</p>
        <div class="hero__buttons">
          <router-link to="/" class="hero__button">Explore</router-link>
          <router-link to="/" class="hero__button">Favourites</router-link>
        </div>
      </div>
      <div class="hero__showcase">
        <img class="hero__img" src="wallpaper.jpg" alt="Final space">
      </div>
    </section>
  </main>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  }
}
</script>

<style scoped>
.home {
  background-image: url('../assets/space.jpg');
  background-size: cover;
  background-position: center;
}
</style>
