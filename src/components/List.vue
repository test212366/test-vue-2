<template>
  <ul>
    <Item v-for="tweet in items" :key="tweet.id" :tweet="tweet" />
  </ul>
</template>

<script>
import Item from "./Item";
export default {
  components: {Item},
  props: {
    items: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>

</style>