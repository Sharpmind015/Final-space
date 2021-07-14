<template>
  <div class="section-card">
    <img :src="image" class="section-card__img" :alt="alt">
    <router-link class="section-card__title">{{title}}</router-link>
  </div>
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
  background-color: #171313;
  overflow: hidden;
  display: flex;
}

.section-card:before {
  position: absolute;
  left: -100px;
  top: -40px;
  width: 100%;
  height: 100%;
  background-color: #277c99;
}

.section-card__title {
  font-size: 1.7rem;
  color: #ffffff;
}
</style>
