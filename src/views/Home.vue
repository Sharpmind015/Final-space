<template>
  <main class="home">
    <section class="hero">
      <div class="hero__content">
        <div class="heading-image">
          <h1 class="hero__heading">
            <div class="line-1">Final</div>
            <div class="line-2">Space</div>
          </h1>
        </div>
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
  min-height: 90vh;
  padding: 2rem 1.4rem;
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
  width: 350px;
  height: 350px;
  border-radius: 50%;
}

.heading-image {
  background-image: url('../assets/space.jpg');
  background-size: contain;
  background-clip: text;
  color: transparent;
  --webkit-text-fill-color: transparent;
}

.hero__heading {
  font-size: 11rem;

  line-height: 1;
}

.line-2 {
  margin-left: 1.5rem;
}

.hero__tagline {
  font-size: 2rem;
  margin-top: 3rem;
  margin-bottom: 2.5rem;
}

.hero__buttons {
  /*margin-top: 2rem;*/
}

.hero__button {
  position: relative;
  color: #fff;
  font-size: 1.7rem;
  padding: 1rem 1.5rem;
  border: 1px solid #277c99;
  color: #277c99;
  overflow-x: hidden;
  transition: color 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  z-index: 0;
}

.hero__button:before {
  content: '';
  position: absolute;
  left: 0;
  right: unset;
  top: 0;
  width: 0;
  height: 100%;
  background-color: #277c99;
  z-index: -1;
  transition: 0.3s cubic-bezier(0.075, 0.82, 0.165, 1);
}

.hero__button:hover {
  color: #fff;
}

.hero__button:hover:before {
  width: 100%;
  right: 0;
  left: unset;
}

.hero__button:nth-child(2) {
  margin-left: 1.2rem;
}




/*Media queries*/

@media screen and (max-width: 768px) {
  .hero__showcase {
    display: none;
  }
  .hero {
    justify-content: center;
  }
  .hero__content {
    flex: 0 0 90%;
    text-align: center;
  }
}

@media screen and (max-width: 360px) {
  .hero__heading {
    font-size: 6rem;
  }
  .hero__button {
    font-size: 1.5rem;
    display: inline-block;
  }
}
</style>
