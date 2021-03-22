<template>
    <div>
        <h1>Microsoft "Safe Link" Link Extractor</h1>
        <input v-model="link" placeholder="https://www.google.com">
        <button v-on:click="extractLink">Extract Link</button>
        <a v-if="extractedLink.length > 0" :href="extractedLink">{{ extractedLink }}</a>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'MicrosoftLinkExtractor',
  data () {
    return {
      extractedLink: ''
    }
  },
  props: {
    link: String
  },
  methods: {
    extractLink: function () {
      const url = new URL(this.link)
      const params = url.searchParams
      const extractedURL = params.get('url')
      if (extractedURL) {
        this.$data.extractedLink = decodeURIComponent(extractedURL)
      }
    }
  }
})
</script>

<style scoped>
.container {
    display: flex;
}
</style>
