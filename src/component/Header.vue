<template>
  <div>
    <h2>Quotes Added</h2>
    <b-progress :value="quoteValue" :max="maxQuotes" class="mb-3 progress" :animated="true"  show-value></b-progress>
 </div>
</template>

<script>
export default {
  props: ['quoteValue', 'maxQuotes'],
  data: function() {
    return {
      animate: true
    };
  }
};
</script>

<style scoped>
div {
  margin: 20px auto;
  width: 100%;
}

.progress {
  width: 100%;
}
</style>