<template>
  <div class="loader">
    <svg width="110" height="110">
      <circle cx="55" cy="55" r="50" stroke-width="5" stroke="#277c99" fill="transparent"></circle>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Loader'
}
</script>


<style scoped>
.loader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #121212;
}

.loader circle {
  stroke-dasharray: 314.159;
  stroke-dashoffset: 314.159;
  /*animation: circle .6s cubic-bezier(0.075, 0.82, 0.165, 1) 0s 1 infinite alternate running;*/
  /*animation: circle .8s cubic-bezier(0.075, 0.82, 0.165, 1) 0 infinite alternate forwards;*/
  animation-name: circle;
  animation-duration: 1s;
  animation-timing-function: cubic-bezier(0.445, 0.05, 0.55, 0.95);
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

@keyframes circle {
  to {
    stroke-dashoffset: 0;
  }
}
</style>
