<template>
  <div id="app">
    <MicrosoftLinkExtractor />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MicrosoftLinkExtractor from './components/MicrosoftLinkExtractor.vue'

export default Vue.extend({
  name: 'App',
  components: {
    MicrosoftLinkExtractor
  }
})
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
