<template>
  <form @submit.prevent>
    <input
      class="form-input"
      type="text"
      placeholder="Add title"
      v-model="post.title"
      @input="post.title = $event.target.value"
    />
    <input
      class="form-input"
      type="text"
      placeholder="Add text"
      v-model="post.body"
      @input="post.body = $event.target.value"
    />
    <custom-button
      class="submit-button"
      @click="createPost"
    >
      Add post
    </custom-button>
  </form>
</template>

<script>
export default {
  emits: ['create-new-post'],
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now()
      this.$emit('create-new-post', this.post)
      this.post = {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}

.form-input {
  width: 100%;
  border: 1px solid olivedrab;
  padding: 10px 15px;
  margin-top: 15px;
}
.submit-button {
    margin-top: 16px;
    align-self: flex-end;
}
</style>
