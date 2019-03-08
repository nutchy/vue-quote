<template>
  <div id="app">
    <div class="container">
      <!-- Heading -->
      <p class="title is-2">Quotes</p>

      <!-- Input Field -->
      <NewQuote @quoteAdded="addQuote"/>

      <!-- Show all quotes -->
      <QuoteGrid :quotes="quotes"/>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'
import NewQuote from './components/NewQuote'

export default {
  name: 'App',
  data: () => {
    return {
      maxQuote: 10,
      quotes: ['Hello']
    }
  },
  methods: {
    addQuote(quote) {
      // quote argument will pass automatically by VueJs
      // in line 8 , another way can use  @quoteAdded="addQuote($event)"
      // but it unnecessary !
      this.quotes.push(quote);
    }
  },
  components: {
    QuoteGrid,
    NewQuote
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
