<template>
  <main class="characters">
    <h1 class="characters__heading">
      <span>/</span> Characters</h1>
    <section class="characters__cards">
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
.characters {
  display: inline-block;
  font-weight: 500;
  margin-left: 4rem;
  padding: 2rem 0.5rem;
}

.characters__heading {
  font-size: 6rem;
}

.characters__heading span {
  color: #277c99;
}

.characters__cards {
  display: flex;
  justify-content: space-between;
  margin-top: 4rem;
}

@media screen and (max-width: 768px) {
  .characters__cards {
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  .characters__heading {
    font-size: 4.2rem;
  }
}

@media screen and (max-width: 340px) {
  .characters__heading {
    margin-left: 1rem;
  }
}

@media screen and (max-width: 300px) {
  .characters__heading {
    font-size: 4rem;
  }
}
</style>
