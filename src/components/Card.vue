<template>
  <router-link :to="title" class="section-card">
    <img loading="lazy" :src="image" class="section-card__img" :alt="alt">
    <p class="section-card__title">{{title.toUpperCase()}}</p>
  </router-link>
</template>


<script>
export default {
  name: 'Card',
  props: ['status', 'image', 'name', 'origin']
}
</script>

<style scoped>

</style>
