<template>
  <div id="app">
    <TweetContainer></TweetContainer>
  </div>
</template>

<script>
import TweetContainer from './components/TweetContainer.vue'

export default {
  name: 'App',
  components: {
    TweetContainer
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgba(28, 28, 31, 0.898);
}
</style>
