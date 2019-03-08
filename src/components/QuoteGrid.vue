<template>
  <div class="columns is-multiline">
    <Quote v-for="(quote, index) in quotes" :key="index" @dblclick.native="deleteQuote(index)">
          {{ quote }}
    </Quote>
  </div>
</template>

<script>
import Quote from './Quote'

export default {
  props: ['quotes'],
  components: {
    Quote
  },
  methods: {
    // Add modifier 'native' (from @dblclick to @dblclick.native)
    // when we create custom element
    deleteQuote(index) {
      // Can remove element from this component because `quotes` prop refereces to parent component.
      // but in other hand if we want to refactor code, can use $emit to sent `index` from child component
      // to parant component. it will be better to read and understand

      // The second parameter of splice is the number of elements to remove (Count from that index)
      this.quotes.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
