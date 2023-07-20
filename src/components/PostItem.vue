<template>
  <div class="post">
    <div>
      <div><strong>Title:</strong> {{ post.title }}</div>
      <div><strong>Text:</strong> {{ post.body }}</div>
    </div>
    <div class="post__btns">
      <custom-button> Delete </custom-button>
    </div>
  </div>
</template>

<script>
import CustomButton from '@/components/UI/CustomButton.vue'

export default {
  components: { CustomButton },
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 16px;
  padding: 16px;
  border: 2px solid olivedrab;
}
</style>
