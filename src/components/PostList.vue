<template>
  <div>
    <h3>Posts list</h3>
  </div>
    <post-item
      v-for="post in posts"
      :post="post"
    />
</template>

<script>
import PostItem from "@/components/PostItem.vue";
export default {
  components: {
    PostItem
  },
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
};
</script>

<style scoped>

</style>
