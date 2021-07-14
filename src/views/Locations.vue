<template>
  <main class="locations">
    <h1 class="locations__heading">
      <span>/</span> Locations</h1>
    <section class="locations__cards">
      <Card v-for="(location, index) in locations" :key="index" :type="location.type" :name="location.name" :image="location.image" />
    </section>
  </main>
</template>

<script>
import Card from '@/components/Card';
export default {
  name: 'Locations',
  data() {
    return {
      locations: [
        {
          name: 'Earth',
          type: 'Planet',
          image: 'wallpaper.jpg'
        },
        {
          name: 'Quinn ergon',
          type: 'Alive',
          image: 'wallpaper.jpg'
        }
      ]
    }
  },
  components: {
    Card
  }
}
</script>


<style scoped>
.locations {
  display: inline-block;
  font-weight: 500;
  margin-left: 4rem;
  padding: 2rem 0.5rem;
}

.locations__heading {
  font-size: 6rem;
}

.locations__heading span {
  color: #277c99;
}

.locations__cards {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-top: 4rem;
}

@media screen and (max-width: 768px) {
  .locations__cards {
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  .locations__heading {
    font-size: 4.5rem;
  }
}

@media screen and (max-width: 340px) {
  .locations__heading {
    margin-left: 1rem;
  }
}

@media screen and (max-width: 300px) {
  .locations__heading {
    font-size: 4rem;
  }
}
</style>
