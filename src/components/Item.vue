<template>
  <li >
    <span v-text="tweet.date"></span>
    <p v-text="tweet.body"></p>
  </li>
</template>

<script>
export default {
  props: {
    tweet: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>