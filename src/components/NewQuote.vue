<template>
  <div class="columns">
    <div class="column is-half is-offset-3">
      <div class="field">
        <div class="control">
          <input class="input is-large"
            type="text" placeholder="Type your quote :)"
            v-model="inputText" @keypress.enter="addQuote">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      inputText: ''
    }
  },
  methods: {
    addQuote() {
      this.$emit('quoteAdded', this.inputText)
      this.inputText = ''
    }
  }
}
</script>

<style>

</style>
