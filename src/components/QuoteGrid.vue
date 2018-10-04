<template>
  <div class="row">
    <app-quote v-for="(quote, index) in quotes" v-bind:key="index" @click.native="deleteQuote(index)">{{ quote }}</app-quote>
  </div>
</template>
<script>
import appQuote from './Quote.vue'

export default {
  props: ['quotes'],
  components: {
    appQuote,
  },
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDeleted', index)
    },
  },
}
</script>

<style scoped>
</style>
