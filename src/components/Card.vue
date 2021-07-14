<template>
  <div class="section-card">
    <img loading="lazy" :src="image" class="section-card__img" :alt="name">
    <p class="section-card__title">{{name.toUpperCase()}}</p>
  </div>
</template>


<script>
export default {
  name: 'Card',
  props: ['status', 'image', 'name', 'origin']
}
</script>

<style scoped>

</style>
