<template>
  <router-link :to="title" class="section-card">
    <img loading="lazy" :src="image" class="section-card__img" :alt="alt">
    <p class="section-card__title">{{title}}</p>
  </router-link>
</template>


<script>
export default {
  name: 'SectionCard',
  props: ['image', 'alt', 'title']
}
</script>

<style scoped>
.section-card {
  position: relative;
  flex: 0 0 45%;
  border: 1px solid #277c99;
  overflow: hidden;
  display: flex;
  align-items: center;
}

.section-card:hover .section-card__img {
  transform: skew(-2deg) translateX(-10px) scale(1.02);
}

.section-card:hover .section-card__title {
  transform: translateX(10px);
}

.section-card__img {
  object-fit: cover;
  width: 200px;
  height: 150px;
  transition: transform 0.3s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.section-card__title {
  font-size: 1.7rem;
  color: #ffffff;
  padding-left: 2rem;
  transition: transform 0.3s cubic-bezier(0.165, 0.84, 0.44, 1);
}
</style>
