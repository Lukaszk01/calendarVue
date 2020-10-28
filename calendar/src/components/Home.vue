<template>
  <div id="home">
    <h2>Hello</h2>
  </div>
</template>

<script>
import Home from './components/Home.vue'
export default {
  name: 'home',
  components: {
    Home
  }
}
</script>

<style>
#home {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
