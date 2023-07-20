<template>
  <div class="app">
    <form>
      <input
        class="form-input"
        type="text"
        placeholder="Add title"
        v-bind:value="post.title"
        @input="onInputTitleChange"
      >
      <input
        class="form-input"
        type="text"
        placeholder="Add text"
        v-bind:value="post.body"
        @input="onInputBodyChange"
      >
      <button
        type="submit"
        class="submit-button"
        @click="createPost">
        Add post
      </button>
    </form>

      <div class="post" v-for="post in posts">
        <div><strong>Title:</strong> {{post.title}}</div>
        <div><strong>Text:</strong> {{post.body}}</div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      posts: [
        {id: 1, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
        {id: 2, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
        {id: 3, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
      ],
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost () {

    },
    onInputTitleChange (event) {
      this.post.title = event.target.value
    },
    onInputBodyChange (event) {
      this.post.body = event.target.value
    }
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
.app{
    padding: 24px;
}
form{
    display: flex;
    flex-direction: column;
}
.post {
    margin-top: 16px;
    padding: 16px;
    border: 2px solid olivedrab;
}
.form-input{
    width: 100%;
    border: 1px solid olivedrab;
    padding: 10px 15px;
    margin-top: 15px;
}
.submit-button{
    align-self: flex-end;
    margin-top: 16px;
    padding: 8px 16px;
    background: none;
    color: olivedrab;
    border: 1px solid olivedrab;
}
</style>
