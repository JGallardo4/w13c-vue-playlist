<template>
  <main id="app">
		<music-player></music-player>
  </main>
</template>

<script>
import MusicPlayer from "./components/MusicPlayer.vue";

export default {
  name: 'App',
  components: {
		MusicPlayer
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
