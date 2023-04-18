<template>
  <div id="app">
    <music-selection></music-selection>
  </div>
</template>

<script>
import MusicSelection from '@/components/MusicSelection.vue'

export default {
  name: 'App',
  components: {
    MusicSelection
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
