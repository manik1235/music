<template>
  <div id="app">
    <MusicApp/>
  </div>
</template>

<script>
import MusicApp from './components/MusicApp.vue'

export default {
  name: 'app',
  components: {
    MusicApp
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
