<template>
  <div>
    <h3>Quotes Added</h3>
    <div class="progress">
      <div class="progress-bar" role="progressbar" arial-valuenow="60" arial-valuemin="0" aria-valuemax="100"
            :style="{ width: (quoteCount / maxQuotes) * 100 + '%' }">
        {{ quoteCount }} / {{ maxQuotes }}
        {{ (quoteCount / maxQuotes) * 1000 + '%' }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['quoteCount', 'maxQuotes'],
}
</script>
