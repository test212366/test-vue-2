<template>
  <div class="wrapper">
    <div class="wrapper-content">
      <div class="view">
        <div class="container">
          <Form @title="createPost"/>
          <List v-if="items.length > 0" :items="items"/>
          <p v-else> CreatePost</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import List from '@/components/List'
import Form from '@/components/Form'
export default {
  components: {
   List,
    Form
  },
  data() {
    return {
      items: [
        {
          id: 1,
          body: 'hello',
          likes: 123,
          date: new Date(Date.now()).toLocaleString()
        },
        {
          id: 2,
          body: 'hellololo',
          likes: 13,
          date: new Date(Date.now()).toLocaleString()
        },
        {
          id: 3,
          body: '202002',
          likes: 13,
          date: new Date(Date.now()).toLocaleString()
        },
      ]
    }
  },
  methods: {
    createPost(post) {
      return this.items.unshift(post)
    }
  }
}
</script>

<style>

</style>