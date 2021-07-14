<template>
  <main class="explore">
    <h1 class="explore__heading">
      <span>/</span> Explore</h1>
    <section class="explore__sections">
      <SectionCard v-for="section in sections" :key="section.title" :title="section.title" :image="section.image" :alt="section.alt" />
    </section>
  </main>
</template>

<script>
import SectionCard from '@/components/SectionCard';
export default {
  name: 'Explore',
  data() {
    return {
      sections: [
        {
          alt: '',
          image: 'wallpaper.jpg',
          title: 'Locations'
        },
        {
          alt: '',
          image: 'wallpaper.jpg',
          title: 'Characters'
        }
      ]
    }
  },
  components: {
    SectionCard
  }
}
</script>


<style scoped>
.explore {
  min-height: 90vh;
  padding: 2rem 1.7rem;
}

.explore__heading {
  display: inline-block;
  font-size: 6rem;
  font-weight: 500;
  margin-left: 4rem;
  padding: 2rem 0.5rem;
}

.explore__heading span {
  color: #277c99;
}

.explore__sections {
  display: flex;
  justify-content: space-around;
  margin-top: 4rem;
}

@media screen and (max-width: 768px) {
  .explore__sections {
    display: block;
  }
}

@media screen and (max-width: 340px) {
  .explore__heading {
    margin-left: 1rem;
  }
}

@media screen and (max-width: 300px) {
  .explore__heading {
    font-size: 4rem;
  }
}
</style>
