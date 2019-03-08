<template>
  <div class="columns">
    <div class="column is-half is-offset-3">
      <progress class="progress is-info" :value="count" max="10"></progress>
    </div>
  </div>
</template>

<script>
export default {
  props: ['count']
}
</script>

<style>

</style>
