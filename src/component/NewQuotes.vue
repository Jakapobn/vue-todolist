<template>
    <div>
        <h4 class="text-align">Quote</h4>
        <textarea class="textarea" row="3" v-model="quote"></textarea>
        <b-button variant="primary" @click.prevent="createNew" > Add Quote</b-button>
    </div>

    
</template>

<script>
export default {
  props: ['quoteValue'],
  data: function() {
    return {
      quote: ''
    };
  },
  methods: {
    createNew() {
      if (this.quoteValue < 10) {
        if (this.quote !== '') {
          this.$emit('quoteAdd', this.quote);
          this.quote = '';
        }
      } else {
        alert('max of quote!');
      }
    }
  }
};
</script>

<style scoped>
div {
  text-align: center;
  margin: 0 300px auto;
  width: 100%;
}

.text-align {
  text-align: left;
}

.textarea {
  width: 100%;
  height: 100px;
}
</style>
