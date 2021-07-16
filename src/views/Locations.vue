<template>
  <main class="locations">
    <h1 class="locations__heading">
      <span>/</span> Locations</h1>
    <Loader v-if="isLoading" />
    <section class="locations__cards">
      <Card v-for="(location, index) in locations" :key="index" :type="location.type" :name="location.name" :image="location.image" />
    </section>
  </main>
</template>

<script>
import Card from '@/components/Card';
import Loader from '@/components/Loader';
export default {
  name: 'Locations',
  data() {
    return {
      locations: [],
      isLoading: true
    }
  },
  components: {
    Card,
    Loader
  },
  created() {
    fetch('https://finalspaceapi.com/api/v0/location/').
      then(res => res.json()).
      then(res => {

        const mappedRes = res.map(({ name, type, img_url }) => {
          return {
            name,
            type,
            image: img_url
          }
        });
        this.locations = mappedRes;
        this.isLoading = false;

      }).catch(err => { console.log(err) })
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
