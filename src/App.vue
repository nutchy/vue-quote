<template>
  <div id="app">
    <div class="container">
      <!-- Heading -->
      <p class="title is-2">Quotes</p>

      <!-- Input Field -->
      <div class="columns">
        <div class="column is-half is-offset-3">
          <div class="field">
            <div class="control">
              <input class="input is-large"
                type="text" placeholder="Large input"
                v-model="inputText" @keypress.enter="addQuote">
            </div>
          </div>
        </div>
      </div>

      <!-- Show all quotes -->
      <QuoteGrid :quotes="quotes"/>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'

export default {
  name: 'App',
  data: () => {
    return {
      inputText: '',
      maxQuote: 10,
      quotes: ['Hello']
    }
  },
  methods: {
    addQuote() {
      this.quotes.unshift(this.inputText);
    }
  },
  components: {
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
