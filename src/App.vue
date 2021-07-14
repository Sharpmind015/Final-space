<template>
  <div class="main">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
export default {
  name: 'App',
  components: { Header }
}
</script>


<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-size: 62.5%;
}

body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

a {
  text-decoration: none;
}

ul,
li {
  list-style: none;
}
</style>
