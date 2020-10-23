<template>
  <div id="app">
  <SingleLED></SingleLED>
  </div>
</template>

<script>
import SingleLED from './components/Single LED.vue'

export default {
  name: 'App',
  components: {
    SingleLED
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
