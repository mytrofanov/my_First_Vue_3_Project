<template>
  <div class="post" v-for="post in posts">
    <div><strong>Title:</strong> {{post.title}}</div>
    <div><strong>Text:</strong> {{post.body}}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
};
</script>

<style scoped>
.post {
  margin-top: 16px;
  padding: 16px;
  border: 2px solid olivedrab;
}
</style>
