<template>
  <div class="app">
    <post-form
      @create-new-post="addPost"
    />
    <post-list
      :posts="posts"
    />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostForm, PostList
  },
  data () {
    return {
      posts: [
        {id: 1, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
        {id: 2, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
        {id: 3, title: 'Some title', body: 'Some text alsdkjfl jvlkalf nvlnla lanfn lvnflnad'},
      ],
    }
  },
  methods: {
    addPost (newPost) {
      this.posts = [newPost, ...this.posts]
    },
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

</style>
