<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="inputValue" required>
    <button type="submit">Add</button>
  </form>
</template>

<script>
export default {
  data() {
    return{
      inputValue: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('title', {
        id: Math.round(Math.random()* 30),
        body: this.inputValue,
        likes: 123,
        date: new Date(Date.now()).toLocaleString()
      })
      this.inputValue = ''
    }
  }

}
</script>

<style scoped>

</style>