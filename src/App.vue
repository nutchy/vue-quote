<template>
  <div id="app">
    <QuoteGrid>
      <Quote :text="quotes[0]"/>
    </QuoteGrid>
  </div>
</template>

<script>
import Quote from './components/Quote'
import QuoteGrid from './components/QuoteGrid'

export default {
  name: 'App',
  data: () => {
    return {
      maxQuote: 10,
      quotes: ['Hello World']
    }
  },
  components: {
    Quote,
    QuoteGrid
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
