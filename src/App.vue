<template>
  <div class="container">
    <div class="row">
        <app-header :quoteValue="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote  @quoteAdd="newQuote" :quoteValue="quotes.length" ></app-new-quote>
        <app-quotes v-for="(quote,index) in quotes" :key="quote" @click.native="deleteQuote(index)">{{quote}}</app-quotes>
    </div>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it ! </div>
      </div>
    </div>
  </div>
</template>

<script>
import Quotes from './component/quotes.vue';
import Header from './component/header.vue';
import NewQuote from './component/newquotes.vue';

export default {
  data: function() {
    return {
      quotes: ['new quote'],
      maxQuotes: 10
    };
  },
  components: {
    appQuotes: Quotes,
    appHeader: Header,
    appNewQuote: NewQuote
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style lang="scss">
.container {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
