<template>
  <div class="loader">
    <svg width="210" height="210">
      <circle cx="105" cy="105" stroke-width="60" stroke="#277c99" fill="transparent"></circle>
    </svg>
  </div>
</template>


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
}

.loader circle {
  stroke-dasharray: 628.319;
  stroke-dashoffset: 628.319;
  animation: circle .6s cubic-bezier(0.075, 0.82, 0.165, 1) 0s 1 infinite alternate running;
  /*animation: name duration timing-function delay iteration-count direction fill-mode;*/
}

@keyframes circle {
  to {
    stroke-dasharray: 0;
  }
}
</style>
