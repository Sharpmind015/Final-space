<template>
  <main class="location">
    <h1 class="location__heading">
      <span>/</span> Explore</h1>
    <section class="location__cards">
      <Card v-for="(character, index) in characters" :key="index" :status="character.status" :name="character.name" :image="character.image" :origin="character.origin" />
    </section>
  </main>
</template>

<script>
import Card from '@/components/Card';
export default {
  name: 'Characters',
  data() {
    return {
      characters: [
        {
          name: 'Gary goodspeed',
          status: 'Alive',
          origin: 'Earth',
          image: 'wallpaper.jpg'
        },
        {
          name: 'Quinn ergon',
          status: 'Alive',
          origin: 'Earth',
          image: 'wallpaper.jpg'
        },
      ]
    }
  },
  components: {
    Card
  }
}
</script>


<style scoped>
.location {
  display: inline-block;
  font-size: 6rem;
  font-weight: 500;
  margin-left: 4rem;
  padding: 2rem 0.5rem;
}

.location__heading span {
  color: #277c99;
}

.location__cards {
  display: flex;
  justify-content: space-between;
  margin-top: 4rem;
}

@media screen and (max-width: 768px) {
  .location__cards {
    display: block;
  }
}

@media screen and (max-width: 340px) {
  .location__heading {
    margin-left: 1rem;
  }
}

@media screen and (max-width: 300px) {
  .location__heading {
    font-size: 4rem;
  }
}
</style>
