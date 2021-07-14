<template>
  <div class="card">
    <img loading="lazy" :src="image" class="card__img" :alt="name">
    <div class="card__content">
      <h5 class="card__title">{{name}}</h5>
      <p class="card__status">{{status}}</p>
      <p class="card__origin">{{origin}}</p>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Card',
  props: ['status', 'image', 'name', 'origin']
}
</script>

<style scoped>
.card {
  position: relative;
  width: 150px;
  min-height: 200px;
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  border-radius: 25px;
  color: #333;
  transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.card:hover {
  transform: translateY(-7px);
}

.card__img {
  height: 60%;
  object-fit: cover;
  max-width: 100%;
  border-radius: 0 25px;
}

.card__content {
  padding: 0.5rem 0.5rem 0 1.9rem;
}

.card__content p,
.card__content h5 {
  margin-top: 0.8rem;
}

.card__title {
  font-size: 1.3rem;
}
</style>
