<template>
  <div class="columns is-multiline">
    <Quote v-for="(quote, index) in quotes" :key="index">
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
  }
}
</script>

<style>

</style>
