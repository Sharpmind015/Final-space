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
  min-height: 90vh;
}

.hero {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100vw;
  height: 100%;
}

.hero__showcase {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.hero__showcase,
.hero__content {
  flex: 0 0 45%;
}

.hero__img {
  object-fit: cover;
  width: 300px;
  height: 300px;
  border-radius: 50%;
}
</style>
